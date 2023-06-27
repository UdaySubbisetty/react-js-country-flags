# react-country-flag

> React component for country flags/details.

[![NPM](https://img.shields.io/npm/v/react-country-flag.svg)](https://www.npmjs.com/package/react-country-flag)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install
## Result 
<img src="./Result.png" alt="Result.png" width="80%" />

## Usage

Pass the country code or dial_code to get details/flag/flag emoji

```jsx
import React from "react"
import {getFlagsByDialCode,getFlagByCountryName,getFlagEmojiByCountryName,getCountryDetailsByName} from "react-js-country-flags";

function App() {

  const countryList1 = getFlagsByDialCode("+1")
  const countryList91 = getFlagsByDialCode("+91")
  return (
    <div className="App" style={{padding:"10px"}}>
      <p>Country flag by dial code +1 : {JSON.stringify(countryList1)}</p>
      {countryList1.map((country)=> <img key={country.dial_code} src={country.flag} style={{height:'30px',width:'30px',marginRight:'10px'}}/>)}
      <br/>

      <p>Country flag by dial code +91 : {JSON.stringify(countryList91)}</p>
      {countryList91.map((country)=> <img key={country.dial_code} src={country.flag} style={{height:'30px',width:'30px',marginRight:'10px'}}/>)}
      <br/>

      <p>Country flag by name US</p>
       <img src={getFlagByCountryName("US")} style={{height:'30px',width:'30px'}}/>
      <br/>
 
      <p>country Emoji {getFlagEmojiByCountryName("in")}</p>


      <p>Country details by name IN : {JSON.stringify(getCountryDetailsByName("in"))}</p>
     
      <br/>

    </div>
  );
}

export default App;
```

# Detecting Emoji support

Try this out and conditionally render your country flag
https://github.com/danalloway/detect-emoji-support

## License

MIT © [UdaySubbisetty](https://github.com/UdaySubbisetty)
