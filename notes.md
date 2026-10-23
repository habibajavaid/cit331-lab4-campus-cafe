# HTTP observations (Lab 4, Task 1)
 
| Question | My answer |
|----------|-----------|
| Request method for index.html | In the request method for index.html we saw the
 Request URL
http://127.0.0.1:5500/index.html
Request method
GET
Status code
200 OK
Remote address
127.0.0.1:5500
Referrer policy
strict-origin-when-cross-origin|


| Status code with Disable cache ticked | When we disable the cache ticked .. show index.html and request tabe see that 304 occur mean it not modified show in the status code. |


| Status code on a normal reload | On norma reload the status code is 200 ok. |


| Status code for /nothing-here.html |In which different status code show and in index.html show 200 OK (from prefetch cache)|


| Value of the Content-Type response header | content-type
text/html; charset=utf-8|

| Remote Address (IP and port) | 
216.239.34.157:443|     in which 216.239.34.157 is the IP and port : 443


| Protocol in the address bar (http or https) | The Protocol is https (443)|.
 
## Why is this address http and not https?
... (This address use HTTP beacuse 127.0.0.1 point to my own computer so the traffic never leave my machine and , never across the network where someone could spy on it. HTTPS only protects data while it travels across a network, so for local traffic it isn’t needed.)




## Specificity Experiment
An ID selector (`#main p`) overrides a class and element selector (`.hero p`), even if the class comes later in the CSS file. When I changed it to `main p`, the hero paragraph went back to white because the class selector won.

## Selectors I used
| Selector kind | Example from my CSS |
| :--- | :--- |
| Element | `body` |
| Class | `.card` |
| ID | `#main` |
| Grouping (comma) | `h1, h2, h3` |
| Descendant (space) | `.nav-list a` |
| Child (`>`) | `main > section` |
| Adjacent sibling (`+`) | `h1 + p` |
| Compound (no space) | `a.active` |
| Attribute | `input[required]` |
| Pseudo-class | `:hover` |
| Pseudo-element | `::before` |




## Bug log (Lab 4, Task 6)
 
What was wrong (file and line)	Which tool showed it	My fix
1	HTML link is style.css but file is bugs.css	Network tab (404 error)	Change link href to bugs.css
2	Image is missing an alt attribute	W3C Validator / Lighthouse	Add alt="Campus Cafe logo"
3	The <html> tag is missing lang="en"	Lighthouse / Accessibility	Add lang="en" to <html>
4	Menu uses <div class="menu"> instead of <nav>	Accessibility tree	Change <div> to <nav>
5	Heading jumps from <h1> to <h4>	Accessibility / Validator	Change <h4> to <h2>
6	Label for="mail" doesn't match input id="email"	Lighthouse (Form elements...)	Change for="mail" to for="email"
7	CSS property is spelled colour: #ffffff	Styles pane (yellow warning)	Change to color: #ffffff
8	CSS class is .notes but HTML is class="note"	Styles pane (rule never applies)	Change .notes to .note
9	The <button> is missing type="submit"	Validator / default behavior	Add type="submit"
10	Color contrast on .note (#999999 on white) is too low	Lighthouse	Change color to #555555