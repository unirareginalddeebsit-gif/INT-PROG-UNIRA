###### PRESENTATION SCRIPT 1: STATIC HTML \& CSS WEBSITE (PHASE 1)

Speaker 1 (Main Presenter): Delfino, Prince V.

---

###### Hey guys, good day! Welcome sa aming first presentation. Today, i-walkthrough namin kayo sa Phase 1 ng aming project, which is 'yung static HTML and CSS version ng aming team profile website. Basically, binuo namin ang Phase 1 as a pure front-end visual interface para magkaroon ng initial online identity ang aming group. Ang main goal natin dito is to create a clean, dark-themed aesthetic na nagha-highlight sa pitong members ng aming BSIT team in a modern layout.  

###### 

###### Para makuha 'yung design na 'to, in-organize namin ang buong page gamit ang standard HTML5 tags at dini-designan gamit ang custom CSS. For instance, 'yung background is styled using a radial dot pattern via radial-gradient(#555 1px, transparent 1px) over a dark #1a1a1a background color. Naglagay din kami ng solid #2C2C2C top header with custom letter-spacing para magmukhang professional developer dashboard. 

###### 

&#x20;'Yung alignment ng cards, ginamitan namin ng CSS flexbox layout with justify-content: center and a fixed gap: 25px para mag-responsive wrap siya depende sa screen size ng user. Si Arsley naman for the hardcoded card structure details. 

Speaker 2: De Guzman, Arsley Duane S.

Thanks, Prince! So regarding sa card layout sa Phase 1, 'yung buong HTML structure was completely hardcoded. Every single team member profile was manually written out as its own <div class="card"> container inside our TEAM-PROFILE.html source code. In each card, naglagay kami ng fixed image tag with a height of 200 pixels, plus an .info wrapper for our personal details.  

Lahat ng personal information namin was written line-by-line gamit ang standard paragraphs at bold tags. Included doon 'yung name natin in an <h2> tag, member role, age, location, course, year level, at hobbies. Para medyo interactive 'yung visuals, nag-apply kami ng backdrop blur filter at CSS transition where hovering over a card scales it up by 1.05 times with a box-shadow glow.  

Moving on, si Kiane naman mag-eexplain ng issues regarding code duplication.  

Speaker 3: Gabrillo, Kiane Amer S.

Thanks, Arsley! 'Yung main issue kasi sa Phase 1, because kailangan naming i-duplicate 'yung entire HTML block seven times para sa pitong members, lumobo 'yung HTML file namin into more than 300 lines of code. Kahit mukha siyang maayos sa screen, super repetitive ng code sa background.  

From a usability standpoint, napaka-limited din ng features. Zero JavaScript interactivity tayo dito—walang live search bar, walang dynamic filtering, at walang modal popups. Kung may visitor na gustong humanap ng member from Bayanan, Tunasan, or Poblacion, kailangan nilang isa-isahin visually 'yung cards sa screen.  

Si Sioson naman for the pros, cons, and overall verdict of Phase 1.

Speaker 4: Sioson, King Amir R.

Thanks, Kiane! To evaluate Phase 1, tingnan natin 'yung advantages and disadvantages nito. On the advantage side, super dali niyang i-deploy. Hindi mo kailangan ng local web server like Apache, zero database requirement, and fast mag-load sa browser kasi raw static HTML files lang ang binabasa ng system.  

However, medyo mabigat 'yung disadvantages. From a developer perspective, maintenance is a complete nightmare. Kapag may kailangang baguhin na simpleng hobby or location, kailangan buksan 'yung raw HTML file, hanapin 'yung specific <div> block, and manually edit the code. This completely breaks the DRY principle—Don't Repeat Yourself.  

So our verdict for Phase 1: maganda siya bilang a quick visual prototype or simple landing page. Pero if you are building an application na kailangan ng regular updates at dynamic user interaction, a purely static website is definitely not the better option. That’s why Phase 1 served as our baseline before upgrading to Phase 2.  

PRESENTATION SCRIPT 2: DYNAMIC HTML/CSS/JS/PHP WEB APP (PHASE 2)

Speaker 1 (Main Presenter): Delfino, Prince V.

  Welcome back, guys! For our second presentation, super excited kami i-showcase ang Phase 2, where we totally upgraded our website into a fully dynamic web application using PHP, JavaScript, HTML, and CSS! In-address namin lahat ng code redundancy at limitations mula sa Phase 1 prototype para i-re-engineer 'yung buong system.

  In Phase 2, pinalitan namin 'yung static structure into a single server-side application file called TeamProfile.php. In-upgrade din namin 'yung visual style using a deeper #121212 background theme, a top search bar, and glassmorphic modal popups for a much cleaner user experience. Instead of loading hardcoded HTML cards, the browser now renders content dynamically through backend server execution.

  This architectural pivot allowed us to separate data management from presentation layout. Imbes na nakasulat 'yung details sa loob ng HTML tags, the server processes structured data first before serving the final output to the user. Si Shejann naman for the backend PHP logic.  

Speaker 2: Lomeda, Shejann C.

Thanks, Prince! So on the backend side, 'yung main core ng Phase 2 is our centralized $team\_members associative array in PHP. Each team member is stored as a structured sub-array containing key-value pairs for name, role, age, location, course, year, hobbies, and image URL.

  Instead of copy-pasting seven separate HTML card containers, pinalitan namin ito ng isang PHP foreach ($team\_members as $member) loop. Page load pa lang, the server automatically iterates through the array and generates the card layout dynamically at runtime. In-apply-an din namin ng htmlspecialchars() 'yung text outputs to prevent potential XSS vulnerabilities.  

Moving on, si Carl naman mag-eexplain ng frontend JavaScript features.

---

Speaker 3: Mallari, Carl Michael E.

Thanks, Shejann! On the frontend, nag-integrate kami ng client-side JavaScript for interactivity. Naglagay kami ng real-time search bar with a keyup event listener na nagja-janitor sa cards via the filterMembers() function, hiding or showing cards based on what the user types.  

Plus, pinalitan namin 'yung crowded text on cards into a minimalist preview layout showing just the image, name, role, and a 'View Overview' button. Clicking the button triggers a JavaScript function that extracts the hidden details and displays a smooth modal popup overlay with a blurred backdrop.

Si Reginald naman for the pros, cons, and final verdict. 

Speaker 4: Unira, Reginald Dee L.

Thanks, Carl! Let’s break down the advantages of Phase 2. The biggest benefit here is high maintainability and scalability. We strictly applied the DRY principle—Don't Repeat Yourself. Kapag may bagong member na papasok sa team, mag-a-append lang tayo ng panibagong sub-array sa PHP file, and the foreach loop automatically renders the new card without changing any layout markup. Plus, 'yung JS search and modal dialogs make the site feel like a modern web app.  

For the disadvantages, Phase 2 requires a local PHP web server environment (like XAMPP or Apache) to execute the code, so hindi mo siya ma-o-open by just double-clicking the file in a file explorer. Medyo tumaas din 'yung technical complexity since combined na 'yung server-side PHP logic and client-side JavaScript DOM manipulation.

 Which one is overall better? Hands down, Phase 2 is significantly better for real-world web development. While Phase 1 is fine for basic static displays, Phase 2 gives us a proper software architecture where data, logic, and design are decoupled. It makes the web application faster to maintain, easier to scale, and far more interactive for users. Thank you so much, guys,



---



