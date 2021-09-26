### Hi there 👋

```javascript
const introduction = (personalInfo) => {
  personalInfo.forEach((property) => {
    if (typeof property === 'string') { console.log(`${property}: ${personalInfo[property]}`); }
    else if (Array.isArray(property) { const joinedProperty = property.join(' '); console.log(`${property}: ${joinedProperty}`); } 
    else if (typeof property === 'object') { property.forEach((element) => { console.log(`  ${element}: ${property[element].join(' ')} `) }; ) }
    ) 
  });
};

// contains relevant personal info
// properities: String name, String type, Array languages, Object tools 
const personalInfo = { 
  name: 'Bernie Green',
  type: 'Full Stack',
  languages: ['JavaScript', 'Python'],
  tools: {
    frontEnd: ['HTML', 'CSS', 'SASS', 'React', 'Redux'],
    backend: ['Express', 'Node', 'MongoDB', 'PostGreSQL', 'Mongoose', 'Axios']
  };
};

introduction(personalInfo);
```


<!-- * **Name**: Bernie Green
* **Developer**: Full Stack
* **Languauges**: JS, Python
- **Tools**: 
  - FrontEnd: HTML, CSS, SASS, React, Redux
  - Backend: Express, Node, Mongo, PostGreSQL, Mongoose -->
<!--
**bgreen280/bgreen280** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

