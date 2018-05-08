New context API exercise



- In Header.js use a render callback inside the AuthConsumer and conditionally display a login or logout button and link.

Remember Context Consumers must have a function as their direct child. This will be passed the value from our Provider.

- If you are stuck you can paste in the code below and then finish it off following the comments:

```javascript
{
  ({ isAuth }) => (
      <React.Fragment>
        <h3>
         <Link to="/">
           HOME
         </Link>
        </h3>

        {/* Modify the code here to conditionally render the link and logout button or just the login button */}
           <ul>
             <Link to="/dashboard">
               Dashboard
             </Link>
             <button onClick={logout}>
               logout
             </button>
           </ul>

           <button onClick={login}>login</button>

      </React.Fragment>
    )
}
```

- Now inside Header.js finish off the code and import our AuthConsumer. Use the value of isAuth to conditionally render the link to /dashboard

- Because isAuth is set to false, only the login button will be visible. Try changing the value to true in the state (it’ll switch to the logout button).

- In AuthContext, add the methods login and logout in addition to isAuth in the AuthContext.Provider

- Lets create a ProtectedRoute component:  

Make Landing and Dashboard components. Our dashboard will only be visible when the user is logged in. Just make something simple for both, such as:

```javascript
import React from 'react'
const Dashboard = () => <h2>User Dashboard</h2>
export default Dashboard
```

- Go to ProtectedRoute and implement the missing code
- In App.js add your ProtectedRoute and use it on line 18
