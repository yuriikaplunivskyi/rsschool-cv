## Yurii Kaplunivskyi

#### Contacts:

- **email:** yuriikaplunivskyi@gmail.com

- **telegram:** [@chudrayk](https://t.me/chudrayk)

- **discord:** [yuriikaplunivskyi#6827](https://discord.com/channels/@me)

- **linkedin:** [Yurii Kaplunivskyi](https://www.linkedin.com/in/yurii-kaplunivskyi/)

#### About myself:
I am decent, responsible and communicative with people.
I have good computer skills, basic knowledge of website development using JavaScript.
Very motivated to deepen my knowledge and learn something new.
I also have enough time to fully immerse myself in the learning process.
For my part, I promise to treat education responsibly,
complete all assigned tasks and do not miss classes.
I have long dreamed of changing my major and becoming a professional web developer.
I spend my free time studying the computer science base, various technologies and tools for website development.
This project is extremely important to me, it will help me fill in the gaps and structure my knowledge, gain practical skills, give me the opportunity
communicate with like-minded people, learn from the experience of professional mentors,
raise the level of your knowledge to a new level, learn about development approaches
web applications, create a number of projects for my portfolio and at the end
will give me the opportunity to get an invitation to my dream job.

#### Skills:
- HTML
- CSS(SСSS|SASS)
- JavaScript
- React
- BEM
- Gulp
- Git
- NodeJS

#### Code example:
````
import MaskedInput from "react-input-mask";
import { Link } from 'react-router-dom';
/* import { useForm } from 'react-hook-form'; */
import './form-support.sass';
import React, { useState, useEffect, useCallback } from 'react';

function SupportForm({showAdditionInput, stylePadding}){
    const [textValue, setTextValue] = useState("");
    const handleTextChange = (event) => {
      setTextValue(event.target.value);
    };
    const [ setInputValue] = useState("");
    
    const handleInputChange = (event) => {
      setInputValue(event.target.value);
    };
  
    const [phone, setPhone] = useState("");
    const [error, setError] = useState(false);
    const [isFocused, setIsFocused] = useState(false);
    
    const handleChange = (event) => {
      setPhone(event.target.value);
    };
    
    const validatePhone = useCallback(() => {
      const pattern = /^[0-9]{3}-[0-9]{2}-[0-9]{2}-[0-9]{2}-[0-9]{3}$/;
      return pattern.test(phone);
    }, [phone]);
    
    useEffect(() => {
      const clearErrorStyle = () => {
        setError(false);
      };
    
      const setErrorStyle = () => {
        setError(true);
      };
    
      if (isFocused && !validatePhone()) {
        setErrorStyle();
      } else {
        clearErrorStyle();
      }
    }, [isFocused, validatePhone]);
    
    const errorStyle = {
      borderBottom: error ? '2px solid #F22B2B' : ' 2px solid rgb(0, 0, 118)',
    };
    const errorStyleChb = {
      borderBottom: error ? '2px solid #F22B2B' : ' 2px solid rgb(0, 0, 118)',
      color: error ? '#F22B2B': ""
    };
    
    const inputStyle = isFocused ? errorStyle : {};
    const inputStyleChb = isFocused ? errorStyleChb : {};
  return (



<form className='support__form' /* onSubmit={handleSubmit(onSubmit)} */>

  <div className='input-box'>
  <input id="input_name" 
         className='input input_required'
         type="text"
         name='name'
         pattern="[a-zA-Zа-яА-ЯҐґЄєІіЇї]+$"
         onChange={handleInputChange}
         onFocus={() => setIsFocused(true)}
         onBlur={() => setIsFocused(false)}
         style={inputStyle}
         maxLength="120"
         placeholder="Введіть ім'я"
         required/>
  <span className='input-box_invalid'>*Це поле є обов’язковим до заповнення</span>
</div>
                
                
      <div className='input-box'>
        <input id="input_email"
               className='input'
               type="email"
               onChange={handleInputChange}
               onFocus={() => setIsFocused(true)}
               onBlur={() => setIsFocused(false)}
               style={inputStyle}
               name='email'
               placeholder="E-mail"
               required/>
        <span className='input-box_invalid'>*Невірний формат email</span>
        </div>

        {showAdditionInput && <div className="input-tel">
          <MaskedInput
            id='input-phone'
            mask="999-99-99-99-999"
            maskPlaceholder="XXX-XX-XX-XX-XXX"
            alwaysShowMask={false}
            type="tel"
            name="phone"
            placeholder="Номер телефону"
            minLength="15"
            value={phone}
            onChange={handleChange}
            onFocus={() => setIsFocused(true)}
            onBlur={() => setIsFocused(false)}
            style={inputStyle}
          />
          {error && (
            <span className='input-box_invalid'>*Невірний формат номеру</span>
          )}
          <span className='input-box_span'>*Опціонально</span>
  </div>}
          
          <div className="input-box">
            <textarea id="na" 
                      name="text"
                      value={textValue}
                      onChange={handleTextChange}
                      onFocus={() => setIsFocused(true)}
                      onBlur={() => setIsFocused(false)}
                      style={inputStyle}
                      maxLength="500"
                      required/>
            
            {textValue.length > 0 && <span className='input-box_span'>Не більше 500({textValue.length}) символів</span>}
            <span className='input-box_invalid'>*Це поле є обов’язковим до заповнення</span>
          </div>

          <div className="form__allow">
            <label className="checkbox">
              <input className="input_checkbox" 
                        type="checkbox"
                        onChange={handleChange}
                        onFocus={() => setIsFocused(true)}
                        onBlur={() => setIsFocused(false)}
                        style={inputStyleChb}
                        required/>
              <span>  </span>
              {error && (
              <span className='input-box_invalid' >**Погодження з політикою конфіденційності є обов’язковим</span>)}

              <span className="checkmark"></span>
              <Link className='link' to='/privacypolicy' target="_blank"  ><span className="form__allow_text" >Я погоджуюся з політикою конфіденційності</span></Link>
              </label>
            
          </div>
          
          <input type='submit' className='form__button button' value="Відправити форму"/>

        </form>
 );
}

export default SupportForm;;
````

#### Experience:
The final project of one of the courses I recently completed (HTML, SCSS, JS, JQUERY): 
[here](https://github.com/yuriikaplunivskyi/final_ssu_hw)

#### Education:
- Kharkiv National University of Internal Affairs - 
Bachelor degree in law (2015 - 2017)

- Java course / Privatbank (2021 - 3 months)

- Anti-school english language course, Kharkiv (2021-2021 - 6 months)

- “Web development” by Ivan Petrichenko, Udemy (2022)

- "Introduction to Mobile DevelopmentIntroduction to Mobile Development" Meta - Coursera( Sep 2022 - Sep 2022)

- "Programming with JavaScriptProgramming with JavaScript" Meta - Coursera (Dec 2022 - Feb 2023)

- “Javascript, React” by Ivan Petrichenko, Udemy (2022-2023)

- “Front-end development”, Sigma Software Univesity (October 2022 - February 2023)

#### Languages:
- English (A2)

- Polish (B1)

- Ukrainian (native)

- Russian (fluent)