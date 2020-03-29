<template>
    <div class = 'container'>
        <div class = 'row'>
            <div class = 'col-md-8'>
                <h2>Create an Account</h2>
                <form @submit.prevent = 'registerUser'>
                    <div class = 'form-group'>
                        <label for = 'First Name'> First Name </label>
                        <input type = 'text' name = 'fname' id = 'fname' placeholder = 'Enter First Name' v-model = 'fname' class="form-control"/>
                        <label for = 'Middle Initial'> Middle Initial </label>
                        <input type = 'text' name = 'Mname' id = 'Mname' placeholder = 'Enter First Name' v-model = 'Mname' class="form-control"/>
                        <label for = 'Last Name'> Last Name </label>
                        <input type = 'text' name = 'lname' id = 'lname' placeholder = 'Enter First Name' v-model = 'lname' class="form-control"/>
                        
                        <label for = 'Address'> Address </label>
                        <input type = 'text' name = 'Address' id = 'Address' placeholder = 'Enter First Name' v-model = 'address' class="form-control"/>
                        
                        <label for = 'Birth Date'> Birthday </label>
                        <input type = 'text' name = 'DOB' id = 'DOB' placeholder = 'Enter First Name' v-model = 'DOB' class="form-control"/>

                        <label for = 'Email Address'> Email </label>
                        <input type = 'email' name = 'Email' id = 'Address' placeholder = 'Enter First Name' v-model = 'Email' class="form-control"/>

                        <label for = 'Username'> Username </label>
                        <input type = 'text' name = 'Uname' id = 'Uname' placeholder = 'Enter Username' v-model = 'Uname' class="form-control"/>                                                
                       
                        <label for = 'Password'> Password </label>
                        <input type = 'password' name = 'password' id = 'pword' placeholder = 'Enter Password' v-model = 'password' class="form-control"/>  
                        <br>
            
                        <button type = "reset" class = "cancelbtn">Cancel</button>
                        <button type = "submit" class ="signupbtn">Sign Up</button>
                    </div>
                </form>
            </div>
        </div>
        <footer>
            <br />
            <br />
            <br />
            <br />
            <br />
            <p id = "msg">&copy; Gaming&Esports 2020</p>
            <br />
        </footer>
    </div>
</template>

<script>
//import axios from 'axios'
//import router from '../router'
export default {
	data () {
		return {
            fname:'',
            Mname:'',
            lname:'',
            address:'',
            DOB:'',
            uname:'',
            password:'',
        }
    },
    methods: {
        registerUser() {
            if (this.fname === '') {
                alert('Field is empty = Please enter your First Name.')
            }
            else if (this.Mname === '') {
                alert('Field is empty = Please enter your Middle Name.')
            }
            else if (this.lname === ''){
                alert('Field is empty = Please enter your Last Name.')
            }
            else if (this.address === ''){
                alert('Field is empty = Please enter your Address.')
            }
            else if (this.DOB === ''){
                alert('Field is empty = Please enter your Birthdate.')
            }
            else if (this.uname === ''){
                alert('Field is empty = Please enter your Username.')
            }
            else if (this.password === ''){
                alert('Field is empty = Please enter your Password.')
            }
        }
    }
}
</script>