
![Logo](https://github.com/vinissimus/next-translate/blob/master/images/logo.svg)

    
# Next-translate vs next-i18next

The main reason that I'm using next-translate over next-i18next is because of the size ,
take a look at the following comparison . (714 B saved!)

![image](https://res.cloudinary.com/practicaldev/image/fetch/s--uLWU34bs--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/h8oi7pr43ibm06wd6lf5.jpeg)
next-i18next.js


![image](https://res.cloudinary.com/practicaldev/image/fetch/s--XQptJoWj--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/ti0et3hv1ym9d4mcxqyg.jpeg)
next-translate


## Documentation

[Documentation](https://github.com/vinissimus/next-translate)


**Setup**

`
npm i --save next-translate
`

**File**

i18n.json
`
{
  "locales": ["en", "zh-tw"],
  "defaultLocale": "en",
  "pages": {
    "*": ["common"]
}
`

next.config.js 
`
const nextTranslate = require('next-translate')
module.exports = nextTranslate()
`

One thing to note is that , if you already have configs in next.config.js

try this
`
module.exports = nextTranslation({
    images:{
        domains:['images.unsplash.com']
    }
})
`
