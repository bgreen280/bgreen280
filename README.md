### Hi there 👋
Check out my deats below :) 
```javascript
/**
 * @param {*} personalInfo - object containing list of personal properities
 * @returns string formated as About me Profile
 * Expected Output --> 
 * About Me
 * name: Bernie Green
 * developerType: Full Stack
 * languages: JavaScript Python
 *   frontEnd: HTML CSS SASS React Redux 
 *   backend: Express Node MongoDB PostGreSQL Mongoose Axios 
*/
const introduction = (personalInfo, level = 0) => {

  // output var to store logged personal information
  let output = '';
  
  // add 'About Me' title at level 0
  if (level === 0) { output = 'About Me \n'; };

  // iterate over string properities and add values to output depending on data type
  // string -> key: value
  // array -> key: value1, value2, ..., valueN
  // object -> recurssivly call function and iterate through object. indents line two spaces for each level
  for (let property in personalInfo) {

    // store value for easy access
    const propertyValue = personalInfo[property];

    // initialize string to be updated below
    let string = '';

    // indent string depending on level
    for (let i = 0; i < level; i++) { string += '  '; };
    
    // update string depending on data type
    if (typeof propertyValue === 'string') { string += `${property}: ${propertyValue}`; }
    else if (Array.isArray(propertyValue)) { string += `${property}: ${propertyValue.join(' ')}`; }
    else if (typeof propertyValue === 'object') { output += introduction(propertyValue, level += 1) }
    
    // add new string to output
    output += string + '\n';
  }

  // output final personal Bio
  return output;
};

// contains Bernie Green's personal info
// properities: String name, String type, Array languages, Object tools 
const personalInfo = { 
  name: 'Bernie Green',
  developerType: 'Full Stack',
  languages: ['JavaScript', 'Python'],
  tools: {
    frontEnd: ['HTML', 'CSS', 'SASS', 'React', 'Redux'],
    backend: ['Express', 'Node', 'MongoDB', 'PostGreSQL', 'Mongoose', 'Axios']
  },
};

const introduceSelf = introduction(personalInfo);
export default introduceSelf;
```
