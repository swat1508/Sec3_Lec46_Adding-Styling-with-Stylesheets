Sec3-Lec46 ==> Adding Styling With Stylesheets
==============================================
In src ==> Person folder we will add a new css file Person.css
Now whatever code will write in this won't be scoped in Person component but will be global css code.

Now in Person_Props.js, we will first add className as below :
const personProp = (props) => {
  return (
  <div> ==changes==to==>  <div className="Person">

  and in Person.css
===================
.Person{
  width:60%;
  margin:16px auto;
  border:1px solid #eee;
  box-shadow: 0 2px 3px #ccc;
  padding : 16px;
  text-align: center;
}

However this much is not enough to reflect changes.We need to import this. So
in Person_Prop.js we will add below import code
import './Person.css';
and now it will work

Sec3-Lec47 ==> Working With Inlinne Styles
==========================================
In src => App.js, we will write :

const style = {
        backgroundColor : 'white',
        font:'inherit',
        border:'1px solid blue',
        padding:'8px',
        cursor:'pointer'
    };


and then in same file will add style attrubute to button
<button style={style} onClick=......
This will work
