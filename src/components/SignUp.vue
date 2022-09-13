<template>

    <main class="form-signin w-100 m-auto">
        <img class="mb-4" src="../assets/res-logo.png" alt="" width="100" height="100">
        <h1 class="display-3">Sign Up</h1>
        <form>
            <div class="form-floating">
                <input type="text" class="form-control top" id="floatingName" placeholder="Your Name" v-model="name">
                <label for="floatingName">Your Name</label>
            </div>
            <div class="form-floating ">
                <input type="email" class="form-control mid" id="floatingEmail" placeholder="name@example.com"
                    v-model="email">
                <label for="floatingEmail">Email address</label>
            </div>
            <div class="form-floating">
                <input type="password" class="form-control bottom" id="floatingPassword" placeholder="Password"
                    v-model="password">
                <label for="floatingPassword">Password</label>
            </div>
            <button class="w-100 btn btn-lg btn-primary" type="submit" v-on:click="signUp">Sign in</button>
            <p class="mt-5 mb-3 text-muted">&copy; 2017–2022</p>
        </form>
    </main>
</template>

<script>
export default {
    name: "SignUp",
    data() {
        return {
            name: '',
            email: '',
            password: ''
        }
    },
    methods: {
        signUp() {
            console.warn("signup", this.name,this.email,this.password);
        }
    }
}
</script>

<style>
.form-signin {
    max-width: 330px;
    padding: 15px;
}

.form-signin .form-floating:focus-within {
    z-index: 2;
}

.top {
    margin-bottom: -1px;
    border-bottom-right-radius: 0;
    border-bottom-left-radius: 0;
}

.mid {
    border-radius: 0;
    margin-bottom: -1px;

}

.bottom {
    margin-bottom: 10px;
    border-top-left-radius: 0;
    border-top-right-radius: 0;
}
</style>