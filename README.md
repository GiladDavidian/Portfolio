"# Portfolio" 

**English**

# Personal Portfolio - Projects

This HTML and CSS project serves as a personal portfolio or landing page showcasing the developer's projects, personal information, and contact options. The design is responsive and adapts to various screen sizes.

## Project Structure

The HTML file (`index.html` or the name you saved the code as) contains the following semantic structure:

* **`<header class="container">`:**
    * **`.hamburger-menu`:** Contains the hamburger button (`.hamburger-button`) and the checkbox (`#menu-toggle`) to control the mobile menu.
    * **`<nav class="mobile-nav">`:** Navigation menu that appears on small screens when the hamburger button is clicked. Includes internal links to different sections of the page.
    * **`<nav class="desktop-nav">`:** Fixed navigation menu displayed on larger screens. Includes an unordered list (`<ul class="navList">`) with internal links.
* **`<div id="header2">`:**
    * Main heading `<h1>פרוייקט HTML+CSS</h1>` (HTML+CSS Project).
    * Paragraph text `<p>` providing general information about the project and the developer's vision.
* **`<div id="programmingLanguages">`:**
    * A collection of SVG icons representing programming languages (HTML, CSS, JavaScript, React). Each icon is a potential link (though not defined as such in the current code).
* **`<div id="mySelf">`:**
    * Personal image `<img>`.
    * Heading `<h1>קצת עליי:</h1>` (About Me).
    * Paragraph text `<p>` with personal information about the developer.
    * Link to download a resume (`<a class="resume">`) from a DOCX file.
    * Link to a separate chatbot page (`<a class="chatBot">`) that opens in a new tab.
* **`<section id="projects">`:**
    * Contains several project boxes (`<div class="boxProject">`).
    * Each box includes:
        * Project image `<img>`.
        * Heading `<h1>` with the project name.
        * Link (`<a>`) to a detailed project page (`portfolioProjectX.html`) that opens in a new tab.
* **`<div class="bgImgForm">` / `<div id="containerForm">`:**
    * Contains a contact form (`<form>`).
    * Heading `<h1>צור קשר</h1>` (Contact Us).
    * Short paragraph text `<p>`.
    * Labels (`<label>`) and input fields (`<input type="text">`) for full name, email, phone, and description.
    * Submit button (`<input type="button" value="שליחה" class="buttonInput">`) (no action defined in the current code).
* **`<footer id="contact">`:**
    * Contains links to various contact methods:
        * Phone (`<a>` with `tel:` scheme).
        * Email (`<a>` with `mailto:` scheme).
        * WhatsApp (`<a>` with a link to WhatsApp Web).
        * LinkedIn (`<a>` with a link to the LinkedIn profile).
    * Each link contains an SVG icon.
* **`<div class="createdBy">`:**
    * Creator note ("Created by©Gilad Davidian").

## Styling (CSS - `style.css`)

The CSS file (`style.css`) provides the styling and layout of the page. Here's an overview of some of the main styles:

* **Basic Style Reset (`*`)**: Removes default margins, padding, and sets `box-sizing` to `border-box` for all elements.
* **Body Styling (`body`)**: Sets the default font (`arial`).
* **Header (`header.container`)**:
    * Black background (`background-color: black`).
    * Fixed position at the top of the page (`position: sticky`, `top: 0`).
    * Uses Flexbox to position the hamburger and desktop menu (`display: flex`, `justify-content: space-between`, `align-items: center`).
    * Internal padding (`padding`).
    * Right-to-left text direction (`direction: rtl`).
* **Desktop Menu (`.desktop-nav`)**:
    * Uses Flexbox (`display: flex`, `flex-grow: 1`, `justify-content: center`).
    * Styles the unordered list (`.navList`) and the links within it (`.desktop-nav ul li a`).
    * Highlights links on hover (`:hover`).
* **Hamburger Menu (`.hamburger-menu`)**:
    * Uses Flexbox (`display: flex`, `align-items: center`, `justify-content: flex-end`).
    * Hides the checkbox (`.menu-toggle`).
    * Styles the hamburger button (`.hamburger-button`) and its three bars (`.bar`).
    * Animates the hamburger on click (changes `transform` and `opacity`).
* **Mobile Menu (`.mobile-nav`)**:
    * Fixed position (`position: fixed`, `top`, `right`).
    * Black background (`background-color: black`).
    * Initial `max-height` of 0 and `overflow: hidden` with a transition (`transition`).
    * Styles the list and links within it.
    * Displays the menu by changing `max-height` when the checkbox is checked (`:checked ~ .mobile-nav`).
* **Main Header Area (`#header2`)**:
    * Sets height and background image (`height`, `background-image`).
    * Centers text (`text-align: center`).
    * Styles the heading and paragraphs.
* **Programming Languages Area (`#programmingLanguages`)**:
    * Uses Flexbox to distribute the icons (`display: flex`, `justify-content: space-evenly`).
    * Styles the size of the SVG icons.
* **"About Me" Area (`#mySelf`)**:
    * Centers text (`text-align: center`).
    * Styles the personal image (size, rounded corners, shadow).
    * Styles the heading and paragraphs.
    * Styles the resume and chatbot links (`.resume`, `.chatBot`) with hover transitions (`transition`, `:hover`).
* **Projects Area (`#projects`)**:
    * Sets background image (`background-image`).
    * Uses CSS Grid (`display: grid`, `grid-template-columns`, `grid-template-rows`, `gap`, `align-items: center`).
    * Styles the project boxes (`.boxProject`) (size, background, shadow).
    * Styles the images, headings, and links within the project boxes, including a hover effect.
* **Contact Form Area (`.bgImgForm`, `#containerForm`, `form`)**:
    * Styles the background of the area and the form (color, image, text direction).
    * Styles the heading, paragraphs, labels, and input fields in the form.
    * Special styling for the description field (`.DescriptionInput`).
    * Styles the submit button (`.buttonInput`) with a hover transition.
* **Contact Information Area (`#contact`)**:
    * Sets height and background (`height`, `background-color`).
    * Uses Flexbox to distribute the icons (`display: flex`, `justify-content: space-around`, `align-items: center`).
    * Styles the size and color of the SVG icons.
* **Creator Area (`.createdBy`)**:
    * Sets height, background, color, and text alignment.
    * Adds internal padding.
* **Media Queries (`@media`)**:
    * Responsive design for smaller screens (up to 576px):
        * Hides the desktop menu and displays the hamburger menu.
        * Changes the project layout to a single column.
        * Adjusts the width of project boxes and the form.
        * Removes the background image from the contact form.
    * Responsive design for larger screens (minimum 576px):
        * Hides the hamburger menu and displays the centered desktop menu.

## Usage

This HTML file, along with the linked CSS file (`style.css`) and the images directory (`images/`), creates an interactive website.

* **Navigation:** The menus (hamburger on small screens and regular menu on large screens) allow quick navigation between different sections of the page using internal links (anchor links).
* **Projects:** Each project is displayed in a separate box with an image and a link to a more detailed page.
* **Contact Us:** The form allows visitors to leave their contact information (additional server-side or JavaScript code is needed to process the form data).
* **External Links:** There are links to download a resume, to a chatbot, and to social media profiles.
* **Responsiveness:** The design adapts to different screen sizes using CSS media queries, ensuring a good user experience on mobile devices and computers.

## Technologies Used

* **HTML5:** Used to create the semantic structure and content of the page.
* **CSS3:** (in `style.css`) Used for advanced styling, flexible layout (Flexbox and Grid), and creating responsiveness.
* **SVG:** Used to display icons and vector graphics, allowing for scaling without loss of quality.

## Notes

* Ensure that the CSS file (`style.css`) and the images directory (`images/`) are in the same directory or the correct path relative to the HTML file for the styling and images to be displayed properly.
* The links to the projects (`portfolioProjectX.html`) and the chatbot (`chatBot.html`) imply the existence of additional HTML files in the project.
* The "Contact Us" form does not include data handling or server-side submission in the current HTML code. Additional code (server-side or JavaScript) is required for it to be functional.
* The WhatsApp link is set up for use with WhatsApp Web. For use with the WhatsApp application on a mobile device, the format might need to be `whatsapp://send?phone=972...`.
* The use of Flexbox and Grid contributes to the flexible and responsive layout of the page elements.
* The hamburger menu is enhanced with CSS (using the `:checked` state of the checkbox) to display and hide the mobile menu with a smooth animation.

This is a detailed README file describing the provided HTML and CSS code. You can add more specific details as needed.

**עברית**

# תיק עבודות אישי - פרוייקטים

פרויקט HTML ו-CSS זה משמש כתיק עבודות אישי או דף נחיתה המציג את הפרויקטים, מידע אישי ואפשרויות יצירת קשר של המפתח. העיצוב רספונסיבי ומתאים לצפייה במגוון רחב של מכשירים.

## מבנה הפרויקט

קובץ ה-HTML (`index.html` או שם אחר בו שמרת את הקוד) מכיל את המבנה הסמנטי הבא:

* **`<header class="container">`:**
    * **`.hamburger-menu`:** מכיל את כפתור ההמבורגר (`.hamburger-button`) ותיבת הסימון (`#menu-toggle`) לשליטה בתפריט הנייד.
    * **`<nav class="mobile-nav">`:** תפריט ניווט המופיע במסכים קטנים כאשר כפתור ההמבורגר נלחץ. כולל קישורים פנימיים לאזורים שונים בדף.
    * **`<nav class="desktop-nav">`:** תפריט ניווט קבוע המוצג במסכים גדולים. כולל רשימה לא מסודרת (`<ul class="navList">`) עם קישורים פנימיים.
* **`<div id="header2">`:**
    * כותרת ראשית `<h1>פרוייקט HTML+CSS</h1>`.
    * פסקת טקסט `<p>` המציגה מידע כללי על הפרויקט והחזון של המפתח.
* **`<div id="programmingLanguages">`:**
    * אוסף של אייקוני SVG המייצגים שפות תכנות (HTML, CSS, JavaScript, React). כל אייקון הוא קישור פוטנציאלי (אם כי לא מוגדר ככזה בקוד הנוכחי).
* **`<div id="mySelf">`:**
    * תמונה אישית `<img>`.
    * כותרת `<h1>קצת עליי:</h1>`.
    * פסקת טקסט `<p>` עם מידע אישי על המפתח.
    * קישור להורדת קורות חיים (`<a class="resume">`) מקובץ DOCX.
    * קישור לעמוד צ'אטבוט נפרד (`<a class="chatBot">`) הנפתח בכרטיסייה חדשה.
* **`<section id="projects">`:**
    * מכיל מספר קופסאות פרויקט (`<div class="boxProject">`).
    * כל קופסא מכילה:
        * תמונה של הפרויקט `<img>`.
        * כותרת `<h1>` עם שם הפרויקט.
        * קישור (`<a>`) לעמוד פרטי של הפרויקט (`portfolioProjectX.html`) הנפתח בכרטיסייה חדשה.
* **`<div class="bgImgForm">` / `<div id="containerForm">`:**
    * מכיל טופס יצירת קשר (`<form>`).
    * כותרת `<h1>צור קשר</h1>`.
    * פסקת טקסט `<p>` קצרה.
    * תוויות (`<label>`) ושדות קלט (`<input type="text">`) לשם מלא, דוא"ל, טלפון ותיאור.
    * כפתור שליחה (`<input type="button" value="שליחה" class="buttonInput">`) (ללא פעולה מוגדרת בקוד הנוכחי).
* **`<footer id="contact">`:**
    * מכיל קישורים לאמצעי יצירת קשר שונים:
        * טלפון (`<a>` עם סכמת `tel:`).
        * דוא"ל (`<a>` עם סכמת `mailto:`).
        * וואטסאפ (`<a>` עם קישור ל-WhatsApp Web).
        * לינקדאין (`<a>` עם קישור לפרופיל לינקדאין).
    * כל קישור מכיל אייקון SVG.
* **`<div class="createdBy">`:**
    * הערת יוצר ("Created by©Gilad Davidian").

## עיצוב (CSS - `style.css`)

קובץ ה-CSS (`style.css`) מספק את העיצוב והסגנון של הדף. להלן סקירה של חלק מהסגנונות העיקריים:

* **איפוס סגנונות בסיסיים (`*`)**: הסרת שוליים, ריפוד והגדרת `box-sizing` ל-`border-box` עבור כל האלמנטים.
* **עיצוב גוף (`body`)**: הגדרת גופן ברירת מחדל (`arial`).
* **כותרת (`header.container`)**:
    * רקע שחור (`background-color: black`).
    * מיקום קבוע בחלק העליון של הדף (`position: sticky`, `top: 0`).
    * שימוש ב-Flexbox כדי למקם את ההמבורגר ותפריט הדסקטופ (`display: flex`, `justify-content: space-between`, `align-items: center`).
    * ריפוד פנימי (`padding`).
    * כיוון טקסט מימין לשמאל (`direction: rtl`).
* **תפריט דסקטופ (`.desktop-nav`)**:
    * שימוש ב-Flexbox (`display: flex`, `flex-grow: 1`, `justify-content: center`).
    * עיצוב רשימה לא מסודרת (`.navList`) והקישורים בתוכה (`.desktop-nav ul li a`).
    * הדגשת קישורים במעבר עכבר (`:hover`).
* **תפריט המבורגר (`.hamburger-menu`)**:
    * שימוש ב-Flexbox (`display: flex`, `align-items: center`, `justify-content: flex-end`).
    * הסתרת תיבת הסימון (`.menu-toggle`).
    * עיצוב כפתור ההמבורגר (`.hamburger-button`) ושלושת הפסים (`.bar`) בתוכו.
    * אנימציה של ההמבורגר בעת לחיצה (שינוי `transform` ו-`opacity`).
* **תפריט נייד (`.mobile-nav`)**:
    * מיקום קבוע (`position: fixed`, `top`, `right`).
    * רקע שחור (`background-color: black`).
    * גובה מקסימלי מאופס (`max-height: 0`, `overflow: hidden`) ומעבר אנימציה (`transition`).
    * עיצוב הרשימה והקישורים בתוכו.
    * הצגת התפריט על ידי שינוי `max-height` כאשר תיבת הסימון מסומנת (`:checked ~ .mobile-nav`).
* **אזור כותרת ראשי (`#header2`)**:
    * גובה ורקע תמונה (`height`, `background-image`).
    * יישור טקסט למרכז (`text-align: center`).
    * עיצוב הכותרת והפסקאות.
* **אזור שפות תכנות (`#programmingLanguages`)**:
    * שימוש ב-Flexbox לפיזור האייקונים (`display: flex`, `justify-content: space-evenly`).
    * עיצוב גודל אייקוני ה-SVG.
* **אזור "קצת עליי" (`#mySelf`)**:
    * יישור טקסט למרכז (`text-align: center`).
    * עיצוב התמונה האישית (גודל, עיגול פינות, צל).
    * עיצוב הכותרת והפסקאות.
    * עיצוב קישורי קורות החיים והצ'אטבוט (`.resume`, `.chatBot`) עם אפקטי מעבר (`transition`) במעבר עכבר (`:hover`).
* **אזור פרויקטים (`#projects`)**:
    * רקע תמונה (`background-image`).
    * שימוש ב-CSS Grid (`display: grid`, `grid-template-columns`, `grid-template-rows`, `gap`, `align-items: center`).
    * עיצוב קופסאות הפרויקט (`.boxProject`) (גודל, רקע, צל).
    * עיצוב התמונות, הכותרות והקישורים בתוך קופסאות הפרויקט, כולל אפקט מעבר במעבר עכבר.
* **אזור טופס יצירת קשר (`.bgImgForm`, `#containerForm`, `form`)**:
    * עיצוב הרקע של האזור והטופס (צבע, תמונה, כיוון טקסט).
    * עיצוב הכותרת, הפסקאות, התוויות ושדות הקלט בטופס.
    * עיצוב מיוחד לשדה התיאור (`.DescriptionInput`).
    * עיצוב כפתור השליחה (`.buttonInput`) עם אפקט מעבר במעבר עכבר.
* **אזור יצירת קשר (`#contact`)**:
    * גובה ורקע (`height`, `background-color`).
    * שימוש ב-Flexbox לפיזור האייקונים (`display: flex`, `justify-content: space-around`, `align-items: center`).
    * עיצוב גודל וצבע אייקוני ה-SVG.
* **אזור יוצר (`.createdBy`)**:
    * גובה, רקע, צבע ויישור טקסט.
    * ריפוד פנימי.
* **שאילתות מדיה (`@media`)**:
    * עיצוב מותאם למסכים קטנים (עד 576px):
        * הסתרת תפריט הדסקטופ והצגת תפריט ההמבורגר.
        * שינוי פריסת הפרויקטים לטור אחד.
        * התאמת רוחב קופסאות הפרויקט והטופס.
        * הסרת תמונת הרקע מטופס יצירת הקשר.
    * עיצוב מותאם למסכים גדולים (מינימום 576px):
        * הסתרת תפריט ההמבורגר והצגת תפריט הדסקטופ הממורכז.

## שימוש

קובץ HTML זה, יחד עם קובץ ה-CSS המקושר (`style.css`) ותיקיית התמונות (`images/`), יוצרים דף אינטרנט אינטראקטיבי.

* **ניווט:** התפריטים (המבורגר במסכים קטנים ותפריט רגיל במסכים גדולים) מאפשרים מעבר מהיר בין חלקי הדף השונים באמצעות קישורים פנימיים (anchor links).
* **פרויקטים:** כל פרויקט מוצג בקופסא נפרדת עם תמונה וקישור לעמוד מפורט יותר.
* **צור קשר:** הטופס מאפשר למבקרים להשאיר פרטים ליצירת קשר (יש צורך בקוד נוסף בצד השרת או JavaScript כדי לעבד את נתוני הטופס).
* **קישורים חיצוניים:** ישנם קישורים להורדת קורות חיים, לצ'אטבוט ולפרופילי מדיה חברתית.
* **רספונסיביות:** העיצוב מותאם לגדלי מסך שונים באמצעות שאילתות מדיה ב-CSS, מה שמבטיח חוויית משתמש טובה במכשירים ניידים ובמחשבים.

## טכנולוגיות בשימוש

* **HTML5:** משמש ליצירת המבנה והתוכן הסמנטי של הדף.
* **CSS3:** (קובץ `style.css`) משמש לעיצוב מתקדם, פריסה גמישה (Flexbox ו-Grid) ויצירת רספונסיביות.
* **SVG:** משמש להצגת אייקונים וגרפיקה וקטורית, המאפשרים קנה מידה ללא פגיעה באיכות.

## הערות

* יש לוודא שקובץ ה-CSS (`style.css`) ותיקיית התמונות (`images/`) נמצאים באותה תיקייה או בנתיב הנכון ביחס לקובץ ה-HTML כדי שהעיצוב והתמונות יוצגו כראוי.
* הקישורים לפרויקטים (`portfolioProjectX.html`) ולצ'אטבוט (`chatBot.html`) מרמזים על קיומם של קבצי HTML נוספים בפרויקט.
* הטופס "צור קשר" אינו כולל טיפול בנתונים או שליחה לשרת בקוד הנוכחי. יש צורך בקוד נוסף (בצד השרת או JavaScript) כדי שהוא יהיה פונקציונלי.
* הקישור לוואטסאפ מוגדר לשימוש ב-WhatsApp Web. לשימוש באפליקציית וואטסאפ במכשיר נייד, ייתכן שיהיה צורך בפורמט `whatsapp://send?phone=972...`.
* השימוש ב-Flexbox וב-Grid תורם לפריסה גמישה ורספונסיבית של רכיבי הדף.
* תפריט ההמבורגר משופר באמצעות JavaScript (באמצעות תיבת הסימון `:checked` ב-CSS) כדי להציג ולהסתיר את התפריט הנייד עם אנימציה חלקה.

זהו קובץ README מפורט המתאר את קוד ה-HTML וה-CSS שסופק. ניתן להוסיף פרטים נוספים בהתאם לצורך.