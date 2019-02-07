<template>
    <div id="login-page">
        <b-container>
            <div v-if="haveAccount">
                <h4>Login</h4>
                <hr>
                <b-form-group>
                    <b-form id="form">
                        <label for="email">Email</label>
                        <b-form-input v-model="login.email" type="email" name="email" placeholder="Enter email here" required>
                        </b-form-input>
                    </b-form>
                    <b-form id="form">
                        <label for="pwd">Password</label>
                        <b-form-input v-model="login.password" type="password" name="password" placeholder="Enter password" required>
                        </b-form-input>
                    </b-form>
                    
                </b-form-group>
                <b-form-checkbox class="mb-2 mr-sm-2 mb-sm-0">Remember me</b-form-checkbox>
                <b-button variant="primary">Login</b-button>
                <p>New user? <span @click="account" style="cursor: pointer; text-decoration: underline;">Register</span> </p>
            </div>
            <div v-else>
                <h4>Register</h4>
                <hr>
                <b-form-group>
                    <b-form id="form">
                        <label for="fname">First name</label>
                        <b-form-input v-model="signup.f_name" type="text" name="first name" placeholder="First name" required>
                        </b-form-input>
                    </b-form>
                    <b-form id="form">
                        <label for="lname">First name</label>
                        <b-form-input v-model="signup.l_name" type="text" name="last name" placeholder="Last name" required>
                        </b-form-input>
                    </b-form>
                    <b-form id="form">
                        <label for="email">Email</label>
                        <b-form-input v-model="login.email" type="email" name="email" placeholder="Enter email here" required>
                        </b-form-input>
                    </b-form>
                    <b-form id="form">
                        <label for="pwd">Password</label>
                        <b-form-input v-model="login.password" type="password" name="password" placeholder="Enter password" required>
                        </b-form-input>
                    </b-form>
                </b-form-group>
                <b-button variant="primary">Register</b-button>
                <p>Already have an account? <span @click="account" style="cursor: pointer; text-decoration: underline;">Login</span> </p>
            </div>
        </b-container>

    </div>
</template>

<script>


export default {
    name: "login",
    data() {
        return {
            haveAccount: true,
            login: {
                email: "",
                password: ""
            },
            signup: {
                f_name: "",
                l_name: "",
                dob: ""
            }
        }
    },
    methods: {
        account() {
            this.haveAccount = !this.haveAccount
        }
    }
}
</script>

<style scoped>
    #login-page {
        /* background: orangered; */
        border: 1px solid  #e85434
;
        border-radius: 5px;
        margin: 30px 300px;
        font-family: 'Raleway', sans-serif;
        box-shadow: 1px 2px 1px  #e85434;
        padding: 20px;
    }
    h4 {
    font-family: 'Cinzel', serif;

    }
    hr {
        margin: 10px 30px;
    }
    
    @media only screen and (max-width: 768px)  {
        #login-page {
            margin: 30px;
        }
    }
    #form {
        text-align: left;
    }
</style>
