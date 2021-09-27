### Hi there! I'm Bernie Green 👋

## I'm a Fullstack Developer from 🇺🇸 based in 🇭🇰 

#### Here's a bit about me
- **Currently**: Resident @ Codesmith
- **Looking to**: Collaborate on Open Source Projects
- **Working on**: Developing a productivity App
- **2021 goal**: &uarr;
- **Fact**: Motorbiking 🏍️ from 🇻🇳 Hanoi &rarr; 🌊 🏞️ Ban Gioc Waterfalls &rarr; 🛣️ Ha Giang Loop &rarr; 🇻🇳 Hanoi *is totally worth it* 

---

### _Languages and Tools_ 💻 🛠️ ⚙️
<img align="left" alt="JavaScript" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/javascript/javascript.png" />
<img align="left" alt="Python" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/python/python.png" />
<img align="left" alt="HTML5" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/html/html.png" />
<img align="left" alt="CSS3" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/css/css.png" />
<img align="left" alt="Sass" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/sass/sass.png" />
<img align="left" alt="Node.js" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/nodejs/nodejs.png" />
<img align="left" alt="React" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/react/react.png" />
<img align="left" alt="Redux" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/redux/redux.png" />
<img align="left" alt="SQL" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/sql/sql.png" />
<img align="left" alt="MySQL" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/mysql/mysql.png" />
<img align="left" alt="MongoDB" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/mongodb/mongodb.png" />
<img align="left" alt="Visual Studio Code" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/visual-studio-code/visual-studio-code.png" />
<img align="left" alt="Git" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/git/git.png" />
<img align="left" alt="GitHub" width="26px" src="https://raw.githubusercontent.com/github/explore/78df643247d429f6cc873026c0622819ad797942/topics/github/github.png" />
<img align="left" alt="Terminal" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/terminal/terminal.png" />

<br />
<br />

---

### Where I live 🏠 online  🖥️ 🌐 🕸️ 
[<img align="left" alt="berniegreen" width="22px" src="https://raw.githubusercontent.com/iconic/open-iconic/master/svg/globe.svg" />][website]
[<img align="left" alt="berniegreen | LinkedIn" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][linkedin]

<!-- 
[<img align="left" alt="berniegreen | YouTube" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/youtube.svg" />][youtube]
[<img align="left" alt="berniegreen | Twitter" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/twitter.svg" />][twitter]
[<img align="left" alt="berniegreen | Instagram" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/instagram.svg" />][instagram]
 -->


<br />
<br />

---

#### Here's a snippet for funs!

```javascript/**
 * @param {*} personalInfo - object containing list of personal properities
 * @returns string formated as About me Profile
 * Expected Output -->    
 * About Me
 * name: Bernie Green
 * developerType: Fullstack
 * location: USA Hong Kong
 * activities: 
 *   currently: Resident @ Codemith
 *   lookingTo: Collaborate on Open Source Projects
 *   workingOn: Develop a productivity App
 *   goal: work "working on"
 *   fact: motorbiking from Hanoi to Ban Gioc Waterfalls to Ha Giang Looop to Hanoi is totally worth it
 * 
 * tools:
 *   languages: JavaScript Python
 *   frontend: HTML CSS SASS React Redux 
 *   backend: Express Node MongoDB PostGreSQL Mongoose Axios 
 *   other: git gitHub VScode Terminal
*/
const introduction = (personalInfo, level = 0) => {
  let output = (level === 0) ? 'About Me \n' : '';
  for (let property in personalInfo) {
    const propertyValue = personalInfo[property];
    let string = (level === 0) ? '' : '  '.repeat(level);
    if (typeof propertyValue === 'string') { string += `${property}: ${propertyValue}`; }
    else if (Array.isArray(propertyValue)) { string += `${property}: ${propertyValue.join(' ')}`; }
    else if (typeof propertyValue === 'object') { string += `${property}: \n${introduction(propertyValue, level + 1)}` }
    output += string + '\n';
  }
  return output;
};

const personalInfo = { 
  name: 'Bernie Green',
  developerType: 'Fullstack',
  location: ['USA', 'Hong Kong'],
  activities: { 
    currently: 'Resident @ Codesmith',
    lookingTo: 'Collaborate on Open Source Projects',
    workingOn: 'Developing a productivity App',
    goal: 'see "working on"',
    fact: 'motorbiking from Hanoi to Ban Gioc Waterfalls to Ha Giang Looop to Hanoi is totally worth it'
  },
  tools: {
    languages: ['JavaScript', 'Python'],
    frontend: ['HTML', 'CSS', 'SASS', 'React', 'Redux'],
    backend: ['Express', 'Node', 'MongoDB', 'PostGreSQL', 'Mongoose', 'Axios'],
    other: ['git', 'gitHub', 'VScode', 'Terminal']
  },
};

const introduceSelf = introduction(personalInfo);
export default introduceSelf;
```


[website]: http://www.berniegreen.com/ 
[linkedin]: https://www.linkedin.com/in/bernardjosephgreen/
<!-- 
[twitter]: 
[instagram]: 
[youtube]: 
 -->
