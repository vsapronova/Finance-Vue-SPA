<template>
    <div id="form_login">
        <form method="post">
            <div class="form-group">
                <input v-model="username" autocomplete="off" autofocus class="form-control" name="username" placeholder="Username" type="text">
            </div>
            <div class="form-group">
                <input v-model="password" class="form-control" name="password" placeholder="Password" type="password">
            </div>
            <button @click.stop.prevent="submit()" class="btn btn-primary" type="submit">Log In</button>
        </form>
        <div id="error" v-for="error in errors" style="margin: 50px; width: 300px; margin-left: 380px" class="alert alert-danger" role="alert" >
                    {{ error }}
        </div>
    </div>
</template>