# frontend-end-exam
<!DOCTYPE html>
<html>
<head>
    <title>React Login</title>
</head>
<body>
    <div id="root"></div>

    <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.de    velopment.js" crossorigin></script>
    <script type="text/babel">
        function App() {
            const [username, setUsername] = React.useState("");
            const [password, setPassword] = React.useState("");
            const [message, setMessage] = React.useState("");

            function login() {
                if (username === "admin" && password === "1234") {
                    setMessage("Login Successful!");
                } else {
                    setMessage("Invalid Username or Password");
                }
            }

            return (
                <div>
                    <h2>Login Form</h2>

                    <input
                        type="text"
                        placeholder="Enter Username"
                        onChange={(e) => setUsername(e.target.value)}
                    /><br/><br/>

                    <input
                        type="password"
                        placeholder="Enter Password"
                        onChange={(e) => setPassword(e.target.value)}
                    /><br/><br/>

                    <button onClick={login}>Login</button>

                    <h3>{message}</h3>
                </div>
            );
        }

        ReactDOM.createRoot(document.getElementById("root"))
            .render(<App />);
    </script>
</body>
</html>
