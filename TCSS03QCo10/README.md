## Tailwind CSS 03
## Chapter 3: Project Pseudo-Classes, Forms & Footer
It is my coding practice with the TUTORIAL of Dave Gray. 

## Source
### Dave Gray 的 Tailwind CSS 資源
https://github.com/gitdagray/tailwind-css-course

### Dave Gray 的 Tailwind CSS 課程
https://youtube.com/playlist?list=PL0Zuz27SZ-6M8znNpim8dRiICRrP5HPft&si=TYz4MlVwoMJZuO69

### Dave Gray 的 YouTube 頻道
https://www.youtube.com/@DaveGrayTeachesCode

## Quick Concept offline
###  1. Intro
        教學影片開頭和介紹

###  2. Welcome

###  3. Project Review
        (1)在 terminal 輸入 npx tailwindcss init
        (2)新增資料夾 build
        (3)新增資料夾 src
        (4)新增 input.css
        (5)新增 base
        (6)新增 components
        (7)新增 utilities
        (8)新增 index.html，修改 index.html
        (9)新增資料夾 img
        (10)新增 rocketride.png, rocketman.png, rocketlaunch.png, rocketdab.png
        (11)新增 favicon.ico
        (12)加入 html 路徑為 ./build/*.html
        (13)在 terminal 輸入 npm init -y
        (14)在 package.json 的 scripts，
        設定 tailwind，指令為 npx tailwindcss -i ./src/input.css -o ./build/css/style.css --watch
        (15)在 terminal 輸入 npm i -D prettier-plugin-tailwindcss
        (16)新增 .gitignore，輸入 node_modules
        (17)在 package.json 的 scripts，
        設定 prettier，指令為 npx prettier --write **/*.html
        (18)在桌面點擊滑鼠右鍵，
        選取個人化，點擊色彩，
        在選擇您的模式，選取淺色或深色

###  4. Start tailwindcss
        在 terminal 輸入 npm run tailwind
        即在 terminal 執行 npx tailwindcss -i ./src/input.css -o ./build/css/style.css --watch

###  5. Testimonials section
        (1)在 id 為 testimonials 的 section元素 加入
        設定 figure 元素的 Class
        新增 my-12 為 
        margin-top: 3rem; /* 48px */
        margin-bottom: 3rem; /* 48px */
        
        (2)設定 blockquote 元素的 Class
        新增 bg-teal-600 為 background-color: rgb(13 148 136);
        新增 dark:bg-black 為 
        @media (prefers-color-scheme: dark) {
                background-color: rgb(0 0 0);
        }
        新增 pl-14 為 padding-left: 3.5rem; /* 56px */
        新增 pr-8 為 padding-right: 2rem; /* 32px */
        新增 py-12 為 
        padding-top: 3rem; /* 48px */
        padding-bottom: 3rem; /* 48px */
        新增 rounded-3xl 為 border-radius: 1.5rem; /* 24px */
        新增 relative 為 position: relative;

        (3)設定 p 元素的 Class，
        新增 text-2xl 為 
        font-size: 1.5rem; /* 24px */
        line-height: 2rem; /* 32px */
        新增 sm:text-3xl 為 
        @media (min-width: 640px) {
                font-size: 1.875rem; /* 30px */
                line-height: 2.25rem; /* 36px */
        }
        新增 items-left 為 text-align: left;
        新增 mt-2 為 margin-top: 0.5rem; /* 8px */
        新增 text-white 為 color: rgb(255 255 255);
        新增 dark:text-slate-400 為 
        @media (prefers-color-scheme: dark) {
                color: rgb(148 163 184);
        }

###  6. Add before and after pseudo-elements
        (1)新增 p 元素的 文字
        Acme has always been there for me. Their Explorer rocket arrived in a wooden crate as expected. Life-long customer! A++ shopping experience.
        設定 p 元素的 Class，
        新增 before:content-['\201C'] 為 
        p::before {
                content: '\201C';
        }
        新增 before:font-serif 為
        p::before {
                font-family: ui-serif, Georgia, Cambria, "Times New Roman", Times, serif;
        }
        新增 before:absolute 為 
        p::before {
                position: absolute;
        }
        新增 before:top-0 為 
        p::before {
                top: 0px;
        }
        新增 before:left-0 為 
        p::before {
                left: 0px;
        }
        新增 before:text-9xl 為 
        p::before {
                font-size: 8rem; /* 128px */
                line-height: 1;
        }
        新增 before:text-white 為 
        p::before {
                color: rgb(255 255 255);
        }
        新增 before:opacity-25 為 
        p::before {
                opacity: 0.25;
        }
        新增 before:transform 為 
        p::before {
                transform: translate(...); /* translateX(0.5rem); translateY(0.5rem); */
        }
        新增 before:translate-x-2 為 
        p::before {
                transform: translateX(0.5rem);
        }
        新增 before:translate-y-2 為 
        p::before {
                transform: translateY(0.5rem);
        }

        (2)設定 p 元素的 Class，
        新增 after:content-['\201D'] 為 
        p::after {
                content: '\201D';
        }
        新增 after:font-serif 為
        p::after {
                font-family: ui-serif, Georgia, Cambria, "Times New Roman", Times, serif;
        }
        新增 after:absolute 為 
        p::after {
                position: absolute;
        }
        新增 after:-bottom-20  為 
        p::after {
                bottom: -5rem /* -80px */;
        }
        新增 after:right-0 為 
        p::after {
                right: 0px;
        }
        新增 after:text-9xl 為 
        p::after {
                font-size: 8rem; /* 128px */
                line-height: 1;
        }
        新增 after:text-white 為 
        p::after {
                color: rgb(255 255 255);
        }
        新增 after:opacity-25 為 
        p::after {
                opacity: 0.25;
        }
        新增 after:transform 為 
        p::after {
                transform: translate(...); /* -translateX(0.5rem); -translateY(0.5rem); */
        }
        新增 after:-translate-x-2 為 
        p::after {
                transform: -translateX(0.5rem);
        }
        新增 after:-translate-y-2 為 
        p::after {
                transform: -translateY(0.5rem);
        }

###  7. Testimonials section continued
        (1)設定 figcaption 元素的 Class，
        新增 italic 為 font-style: italic;
        新增 text-xl 為 
        font-size: 1.25rem; /* 20px */
        line-height: 1.75rem; /* 28px */
        新增 sm:text-2xl 為 
        @media (min-width: 640px) {
                font-size: 1.5rem; /* 24px */
                line-height: 2rem; /* 32px */
        }
        新增 text-right 為 text-align: right;
        新增 mt-2 為 margin-top: 0.5rem; /* 8px */
        新增 text-slate-500 為 color: rgb(100 116 139);
        新增 dark:text-slate-400 為 
        @media (prefers-color-scheme: dark) {
                color: rgb(148 163 184);
        }
        符號和文字 &#8212;Wile E. Coyote, Genius

        (2)在 id 為 testimonials 的 section元素 加入
        設定 figure 元素
        設定 blockquote 元素
        設定 p 元素文字 The Acme Adventurer Rocket has thwarted my Illudium Q-36 Explosive Space Modulator on several occassions. This makes me very, very angry! Nevertheless, K-9 and I have awarded Acme the Martian contract for space exploration rockets based on Acme's quality and sturdy designs.
        設定 span 元素的 Class，
        新增 italic 為 font-style: italic;
        文字 This makes me very, very angry!
        設定 figcaption 元素
        符號和文字 &#8212;Martin The Martian &amp; K-9

        (3)在 id 為 testimonials 的 section元素 加入
        設定 figure 元素
        設定 blockquote 元素
        設定 p 元素符號和文字 I knew I not only wanted &#8212; I needed &#8212; Acme's Infinity Rocket for my mission in space. Acme delivered in one day! Nothing says Take me to your leader like Acme's Infinity Rocket! 💯
        設定 span 元素的 Class，
        新增 italic 為 font-style: italic;
        文字 I needed
        設定 q 元素的 Class，
        新增 italic 為 font-style: italic;
        文字 Take me to your leader
        設定 figcaption 元素
        符號和文字 &#8212;Buzz Lightyear

        (4)在桌面點擊滑鼠右鍵，
        選取個人化，點擊色彩，
        在選擇您的模式，選取淺色
        確認版面格式是否需要調整

        (5)如果 p 元素的 Class 為 
        after:translate-x-2 和 after:translate-y-2，
        修改 after:translate-x-2 為 after:-translate-x-2，
        修改 after:translate-y-2 為 after:-translate-y-2

###  8. Contact Form
        (1)設定 form 元素的 action 為 https://httpbin.org/get
        method 為 get

        (2)設定 form 元素的 Class，
        新增 max-w-4xl 為 max-width: 56rem; /* 896px */
        新增 mx-auto 為 
        margin-left: auto;
        margin-right: auto;
        新增 text-2xl 為 
        font-size: 1.5rem; /* 24px */
        line-height: 2rem; /* 32px */
        新增 sm:text-3xl 為 
        @media (min-width: 640px) {
                font-size: 1.875rem; /* 30px */
                line-height: 2.25rem; /* 36px */
        }
        新增 flex 為 display: flex;
        新增 flex-col 為 flex-direction: column;
        新增 items-start 為 align-items: flex-start;
        新增 gap-4 為 gap: 1rem; /* 16px */

        (3)設定 label 元素的 for 為 subject
        文字 Subject:

        (4)設定 input 元素的 type 為 text
        id 為 subject
        name 為 subject
        require
        minlength 為  3 個字元
        maxlength 為 60 個字元
        placeholder 為 Your Subject

        (5)設定 input 元素的 Class 為
        新增 w-full 為 width: 100%;
        新增 text-black 為 color: rgb(0 0 0);
        新增 text-2xl 為 
        font-size: 1.5rem; /* 24px */
        line-height: 2rem; /* 32px */
        新增 sm:text-3xl 為 
        @media (min-width: 640px) {
                font-size: 1.875rem; /* 30px */
                line-height: 2.25rem; /* 36px */
        }
        新增 p-3 為 padding: 0.75rem; /* 12px */
        新增 rounded-xl 為 border-radius: 0.75rem; /* 12px */
        新增 border 為 border-width: 1px;
        新增 border-solid 為 border-style: solid;
        新增 border-slate-900 為 border-color: rgb(15 23 42);
        新增 dark:border-none 為 
        @media (prefers-color-scheme: dark) {
                border-style: none;
        }

        (6)設定 label 元素的 for 為 message
        文字 Message:

        (7)設定 textarea 元素的 name 為 message
        id 為 message
        cols 預設值為 30 個字元
        rows 預設值為 10 個字元
        placeholder 為 Your Message
        require

        (8)設定 textarea 元素的 Class 為
        新增 w-full 為 width: 100%;
        新增 text-black 為 color: rgb(0 0 0);
        新增 text-2xl 為 
        font-size: 1.5rem; /* 24px */
        line-height: 2rem; /* 32px */
        新增 sm:text-3xl 為 
        @media (min-width: 640px) {
                font-size: 1.875rem; /* 30px */
                line-height: 2.25rem; /* 36px */
        }
        新增 p-3 為 padding: 0.75rem; /* 12px */
        新增 rounded-xl 為 border-radius: 0.75rem; /* 12px */
        新增 border 為 border-width: 1px;
        新增 border-solid 為 border-style: solid;
        新增 border-slate-900 為 border-color: rgb(15 23 42);
        新增 dark:border-none 為 
        @media (prefers-color-scheme: dark) {
                border-style: none;
        }

        (9)設定 button 元素的 Class 為
        新增 bg-teal-700 為 background-color: rgb(15 118 110);
        新增 hover:bg-teal-600 為 
        button:hover {
                background-color: rgb(13 148 136);
        }
        
        新增 active:bg-teal-500 為 
        button:active {
                background-color: rgb(20 184 166);
        }
        新增 text-white 為 color: rgb(255 255 255);
        新增 p-3 為 padding: 0.75rem; /* 12px */
        新增 w-48 為 width: 12rem; /* 192px */
        新增 rounded-xl 為 border-radius: 0.75rem; /* 12px */
        新增 border 為 border-width: 1px;
        新增 border-solid 為 border-style: solid;
        新增 border-slate-900 為 border-color: rgb(15 23 42);
        新增 dark:border-none 為 
        @media (prefers-color-scheme: dark) {
                border-style: none;
        }
        文字 Submit

###  9. Footer
        (1)設定 footer 元素的 id 為 footer
        設定 footer 元素的 Class，
        新增 bg-teal-700 為 background-color: rgb(15 118 110);
        新增 text-white 為 color: rgb(255 255 255);
        新增 text-xl 為 
        font-size: 1.25rem; /* 20px */
        line-height: 1.75rem; /* 28px */

        (2)設定 section 元素的 Class，
        新增 max-w-4xl 為 max-width: 56rem; /* 896px */
        新增 mx-auto 為 
        margin-left: auto;
        margin-right: auto;
        新增 p-4 為 padding: 1rem; /* 16px */
        新增 flex 為 display: flex;
        新增 flex-col 為 flex-direction: column;
        新增 sm:flex-row 為 
        @media (min-width: 640px) {
                flex-direction: row;
        }
        新增 sm:justify-between; 為 
        @media (min-width: 640px) {
                justify-content: space-between;
        }

        (3)設定 address 元素，加入聯絡資訊

        (4)設定 nav 元素的 aria-label 為 footer，
        設定 nav 元素的 Class，
        新增 hidden 為 display: none;
        新增 md:flex 為 
        @media (min-width: 960px) { 
                display: flex;
        }
        新增 flex-col 為 flex-direction: column;
        新增 gap-2 為 gap: 0.5rem; /* 8px */

        (5)設定 a 元素的 Class，
        新增 hover:opacity-90 為
        a:hover {
                opacity: 0.9;
        }

        (6)設定 a 元素的 href 為 #rockets
        文字 Our Rockets

        (7)設定 a 元素的 href 為 #testimonials
        文字 Testimonials

        (8)設定 a 元素的 href 為 #contact
        文字 Contact Us

        (9)設定 div 元素的 Class，
        新增 flex 為 display: flex;
        新增 flex-col 為 flex-direction: column;
        新增 sm:gap-2 為 
        @media (min-width: 640px) {
                gap: 0.5rem; /* 8px */
        }

        (10)設定 p 元素的 Class，
        新增 text-right 為 text-align: right;
        文字和符號 Copyright &copy; 2023

        (11)設定 span 元素的 id 為 year，
        文字 2023

        (12)設定 p 元素的 Class，
        新增 text-right 為 text-align: right;
        文字 All Rights Reserved

### 10. Custom Media Queries
        input.css
        (1)輸入 @layer utilities { ... }
        Class 為 .section-min-height
        新增 min-height 為 calc(100vh - 68px)

        tailwind.config.js
        (2)在 extend 中，
        輸入 screens: {
                "widescreen": { "raw": "(min-aspect-ratio: 3/2)"},
                "tallscreen": { "raw": "(min-aspect-ratio: 1/2)"},
        }

        index.html
        (3)在 id 為 hero 的 section元素，
        修改 section元素的 Class 為
        flex flex-col-reverse justify-center sm:flex-row p-6 items-center gap-8 mb-12 scroll-mt-40 widescreen:section-min-height tailscreen:section-min-height
        新增 widescreen:section-min-height 和 tailscreen:section-min-height

        (4)在 id 為 rockets 的 section元素，
        修改 section元素的 Class 為 p-6 my-12 scroll-mt-20 widescreen:section-min-height tailscreen:section-min-height
        新增 widescreen:section-min-height 和 tailscreen:section-min-height

        (5)在 id 為 testimonials 的 section元素，
        修改 section元素的 Class 為 p-6 my-12 scroll-mt-20 widescreen:section-min-height tailscreen:section-min-height
        新增 widescreen:section-min-height 和 tailscreen:section-min-height

        (6)在 id 為 contact 的 section元素，
        修改 section元素的 Class 為 p-6 my-12 scroll-mt-16 widescreen:section-min-height tailscreen:section-min-height
        新增 widescreen:section-min-height 和 tailscreen:section-min-height