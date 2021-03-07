# My CV
***
## Tselyuk Pavel
### Contacts: 1. e-mail: pavlik_astap@mail.ru
             2. LinkedIn: [https://www.linkedin.com/in/pavel-tselyuk-71892b1a2/]:https://www.linkedin.com/in/pavel-tselyuk-71892b1a2/
***
### About me:
  I'm a student in Belarusian National Technical University for a developer and hope to become one :) For some time I learned JS by myself, but that wasn't enough, so here i am.
  ***
  ### My skills:
    - HTML, CSS
    - JavaScript
    - React
***
### Code Example:
``` 
        class SignIn extends Component {
   constructor(props) {
      super(props);
      this.onSubmit = this.onSubmit.bind(this);
   }

   async onSubmit(formData) {
      let login = document.getElementById('login').value.toLowerCase();
      await this.props.signIn(formData);
      if (!this.props.errorMessage) {
         localStorage.setItem('login', login);
         this.props.history.push('/dashboard');
      }
   }

   render() {
      let { handleSubmit } = this.props;
      return (
         <div className="row">
            <div className="col">
               <form action="" onSubmit={handleSubmit(this.onSubmit)}>
                  <fieldset>
                     <Field
                        name="login"
                        type="text"
                        id="login"
                        label="Enter your login"
                        placeholder="example"
                        component={CustomInput} />
                  </fieldset>
                  <fieldset>
                     <Field
                        name="password"
                        type="password"
                        id="password"
                        label="Enter your password"
                        placeholder="yoursuperawesomepassword"
                        component={CustomInput} />
                  </fieldset>

                  {this.props.errorMessage ?
                     <div className="alert alert-danger">
                        {this.props.errorMessage}
                     </div> :
                     null}

                  <button type="submit" className="btn btn-primary">Sign In</button>
               </form>
            </div>
            <div className="col">
               <div className="text-center">
                  <div className="alert alert-primary">
                     For third-part autentication
                  </div>
               </div>
            </div>
         </div>
      )
   }
}

function mapStateToProps(state) {
   return {
      errorMessage: state.auth.errorMessage
   }
}

export default compose(
   connect(mapStateToProps, actions),
   reduxForm({ form: 'signin' })
)(SignIn)
```
  ***
  ### Education:
  I study in BNTU for a developer. I've passed VRP Consulting courses for Apex programming language. I learned JS for some time on my own.
  ### English level:
  I attended Streamline courses and my english level is about B1+.
