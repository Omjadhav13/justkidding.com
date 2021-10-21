# justkidding.com
<html>
        <body>
            <div class="container">
                <form name="f1" action="#">
                    <table>
                        <tr>
                            <td>Enter Name:</td>
                            <td><input type="text" name="name" id="name" />
                            </td>
                        </tr>
                        <tr>
                            <td>Enter SurName:</td>
                            <td><input type="text" name="surname" id="surname" />
                            </td>
                        </tr>
                        <tr>
                            <td>Enter Email:</td>
                            <td><input type="email" name="email" id="email" />
                            </td>
                        </tr>
                        <tr>
                            <td>Enter Password:</td>
                            <td><input type="password" name="password" id="pass" />
                            </td>
                        </tr>
                        <tr>
                            <td colspan="2"><input type="submit" value="Submit" onclick="validate()" /></td>
                        </tr>
                    </table>
                </form>
            </div>
            <script type="text/javascript">
                let name = document.getElementById("name");
                let surname = document.getElementById("surname");
                let email = document.getElementById("email");
                let pass = document.getElementById("pass");
        
                function validate() {
        
                    if (name.value.length == "") {
                        alert("Pls Enter a valid name")
                    }
                    if (surname.value.length == "") {
                        alert("Pls Enter a valid surname")
                    }
                    var validRegex = /^[a-zA-Z0-9.!#$%&'+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)$/;
                    if (!email.value.match(validRegex)) {
                        alert("Pls Enter a Valid email address!");
                    }
                    if (pass.value.length < 5) {
                        alert("Pls Enter a valid pass of more than 5 letters")
                    }
                    if (pass.value.length > 15) {
                        alert("Pls Enter a valid pass of less than 15 letters")
                    }
                }
            </script>
</body>
</html>
