## week 1 - Server
- general
  - show them how to use eslint and prettier
    - make sure comments do not end up on master or console logs don't end up on master
    - did everyone manage to deploy, I could go through this
    - show them how to use nodemon
- SummerButterfly
  - you don't have any instructions for running your project
  - or how to run the tests
  - comments shouldn't be left in production files
  - show them how to use backtick syntax highlighting
  - could have better naming for this template
  - https://github.com/fac28/SummerButterfly/blob/49c45a54e045e418614c7900cec4f6a36a11028a/templates.js#L52
- HahaHub
  - you use == everywhere, you should always use ===
    - you left a console.log in somewhere
    - we're not to be using frameworks or libraries at this stage of the course
    - in the server, you wouldn't name a folder scripts
    - you don't need to equality check against empty string here, you can just do if(!name)
      - https://github.com/fac28/HahaHub/blob/e90e5a9f461172897cc56b08471ad3ffbf07dcfd/scripts/server.js#L47
    - upRoute and downRoute not being used, should be removed to another branch
- week1-microblogging-fac28
  - here you could do an early return
    - https://github.com/cazanelena/week1-microblogging-fac28/blob/0c66d71187985127f078b6bfdba820e38c7ac5c5/src/server.js#L34-L41
      
## Week 2 - Database
- general
    - show how to do object destructuring
    - this function could do with some refactoring
        - [https://github.com/fac28/DoggyDB/blob/bb0325420ca8094aa2173235a7bc0ec04d1190a9/routes/booking.js#L4-L39](https://github.com/fac28/DoggyDB/blob/bb0325420ca8094aa2173235a7bc0ec04d1190a9/routes/booking.js#L4-L39)
    - you don't want to call a function from the model inside the template file
    - it looks like some teams focused a lot on database, that's definitely okay. I could show how to test the database in isolation (db-issy-tess-tommaso-james)
    - is prettier working for people? I didn't see a config file for it
    - add 'no-console' to rules
- DoggyDB
    - you put `npm start` in instructions but it should be `npm run dev`
    - you could use object destructuring here
        - [https://github.com/fac28/DoggyDB/blob/bb0325420ca8094aa2173235a7bc0ec04d1190a9/routes/bookingForm.js#L15-L19](https://github.com/fac28/DoggyDB/blob/bb0325420ca8094aa2173235a7bc0ec04d1190a9/routes/bookingForm.js#L15-L19)
    - if you only use a variable once then you most of the time you don't need to create a variable
        - [https://github.com/fac28/DoggyDB/blob/bb0325420ca8094aa2173235a7bc0ec04d1190a9/routes/bookingForm.js#L20-L25](https://github.com/fac28/DoggyDB/blob/bb0325420ca8094aa2173235a7bc0ec04d1190a9/routes/bookingForm.js#L20-L25)
    - I wouldn't recommend using `+=` as it's confusing to read
        - you could just put the `content` inside the template string at the same time you're reassigning it
    - values already filled in for making a booking, is it meant to work like that?
    - there are no instructions for seeding the project
    - there are console.log's left in
    - sorting mechanism for bookings is cool 😎
    - I like that you used capital letters for templates 👌🏽
    - great splitting out routes into their own files
- natureBase
    - you don't want to call a function from the model inside the template file
        - [https://github.com/fac28/natureBase/blob/f2903a1389ce41eb665ebb67d7243fdc9dc5efdd/src/templates.js#L99-L132](https://github.com/fac28/natureBase/blob/f2903a1389ce41eb665ebb67d7243fdc9dc5efdd/src/templates.js#L99-L132)
    - if a variable is only used in one place then you probably don't need it
        - [https://github.com/fac28/natureBase/blob/f2903a1389ce41eb665ebb67d7243fdc9dc5efdd/src/routes/add.js#L9-L10](https://github.com/fac28/natureBase/blob/f2903a1389ce41eb665ebb67d7243fdc9dc5efdd/src/routes/add.js#L9-L10)
    - you could use an early return here
        - [https://github.com/fac28/natureBase/blob/f2903a1389ce41eb665ebb67d7243fdc9dc5efdd/src/routes/add.js#L37-L43](https://github.com/fac28/natureBase/blob/f2903a1389ce41eb665ebb67d7243fdc9dc5efdd/src/routes/add.js#L37-L43)
    - I'm not 100% sure here but I think you should be importing the `app` from. `server.js` and then adding doing `const router = app.Router()`
        - [https://github.com/fac28/natureBase/blob/f2903a1389ce41eb665ebb67d7243fdc9dc5efdd/src/routes/add.js#L1-L4](https://github.com/fac28/natureBase/blob/f2903a1389ce41eb665ebb67d7243fdc9dc5efdd/src/routes/add.js#L1-L4)
    - form goes all the way to the bottom when there's an error submitting
    - very cool that values remain even after server-side validation
    - great modularisation of routes
    - no eslint config or prettier config
- db-issy-tess-tommaso-james
    - you could use object destructuring here
        - [https://github.com/fac28/db-issy-tess-tommaso-james/blob/ed2bd472d4bec7668578e1e4a6e1009c5eac5e7b/src/server.js#L24-L28](https://github.com/fac28/db-issy-tess-tommaso-james/blob/ed2bd472d4bec7668578e1e4a6e1009c5eac5e7b/src/server.js#L24-L28)
    - you could have an early return here rather than this `else` block
        - [https://github.com/fac28/db-issy-tess-tommaso-james/blob/ed2bd472d4bec7668578e1e4a6e1009c5eac5e7b/src/server.js#L49-L64](https://github.com/fac28/db-issy-tess-tommaso-james/blob/ed2bd472d4bec7668578e1e4a6e1009c5eac5e7b/src/server.js#L49-L64)
    - when I press submit on the form all the values are wiped if one isn't working, a stretch goal could be to keep the values already entered in there
    - how come the cuisine name has to be unique? surely multiple types of restaurants could have the same type of cuisine
    - you don't have eslint or prettier
    - there are console.log's left in
        - [https://github.com/fac28/db-issy-tess-tommaso-james/blob/ed2bd472d4bec7668578e1e4a6e1009c5eac5e7b/src/server.js#L29](https://github.com/fac28/db-issy-tess-tommaso-james/blob/ed2bd472d4bec7668578e1e4a6e1009c5eac5e7b/src/server.js#L29)
    - there aren't any instructions for seeding the database
    - the instructions for running the database aren't the right ones for dev/local environment (it should be `npm run dev`)
    - cool use of `normalize.css`

## Week 3 - Authentication
- PactPortal
		- you might wanna abstract out a createCookie function so you can have cleaner route and put constant values in one place. (or even just abstract out the cookie options)
			- https://github.com/fac28/PactPortal/blob/901e8b8c05e6d3e1cefe8721f3afaca08262a81e/src/routes/sign-up.js#L30-L35
			- https://github.com/fac28/PactPortal/blob/901e8b8c05e6d3e1cefe8721f3afaca08262a81e/src/routes/log-in.js#L34-L39
		- how come you used `cross-env`?
		- i could show them how to make 'protected-route' middleware
		- i liked how your template and route folder have a similar structure
		- how come you're passing `req` and `res` to both these functions if those arguments aren't being used?
			- https://github.com/fac28/PactPortal/blob/901e8b8c05e6d3e1cefe8721f3afaca08262a81e/src/templates/home.js#L4-L41
		- how are you getting the logs in the console?
		- you can use early return here
			- https://github.com/fac28/PactPortal/blob/901e8b8c05e6d3e1cefe8721f3afaca08262a81e/src/routes/sign-up.js#L23-L44
		- do we want to see how to install husky?
		- in your error handling you could reply with something to the user
			- https://github.com/fac28/PactPortal/blob/901e8b8c05e6d3e1cefe8721f3afaca08262a81e/src/routes/log-in.js#L34-L39
			- show them how to mock errors in the code by just throwing
		- just a matter of stylistic preference but you could combine these two lines into one
			- https://github.com/fac28/PactPortal/blob/901e8b8c05e6d3e1cefe8721f3afaca08262a81e/src/routes/user.js#L15-L16
	- bookmarks2
		- there's similar logic in these two routes, you could abstract it out into middleware
			- https://github.com/fac28/bookmarks2/blob/0e4b53cd8cf3e307f799087156e83c886680ec5d/src/routes/bookpage.js#L1-L46
		- to run locally you do `npm run dev` in your project. if i used `npm start` the env variables wouldn't be set
			- https://github.com/fac28/bookmarks2/blob/0e4b53cd8cf3e307f799087156e83c886680ec5d/README.md?plain=1#L29-L37
		- no eslint or prettier config
		- love how tidy your server file is 😍
		- console.log's left in
		- you don't need an else block here because you've already got an early return
			- https://github.com/fac28/bookmarks2/blob/0e4b53cd8cf3e307f799087156e83c886680ec5d/src/routes/log-in.js#L17-L36
		- how come you use the login routes for `/log-in` endpoint but also for `/my-shelf` endpoints
			- it's a bit confusing that some routes are getting set multiple times
		- `createBook` should probably run with `run` rather than `get` as you're not using the book that's returned
		- love both these early returns on the 'failure' path
			- https://github.com/fac28/bookmarks2/blob/0e4b53cd8cf3e307f799087156e83c886680ec5d/src/routes/bookpage.js#L10-L44
	- play-dates
		- to run locally you do `npm run dev` in your project. if i used `npm start` the env variables wouldn't be set
			- https://github.com/fac28/play-dates/blob/73ed1d513efa40118e8a7a9ce22ced9fdf668058/README.md?plain=1#L36-L38
		- still quite a few console logs left in
		- this isn't doing anything, there is no rule called `prettier/prettier` as far as I know. maybe a confusion between prettier and eslint here
		- love how tidy the server is 😍
		- how come you assign `currentMonth` and then only use it to assign to `month` variable. can't you just call it `month` to start with? (same with year two lines above actually)
			- https://github.com/fac28/play-dates/blob/73ed1d513efa40118e8a7a9ce22ced9fdf668058/src/routes/home.js#L14-L15
		- these lines could come up at the top of the route for greater readability
		  id:: 651dffab-2b1d-476c-9d12-771d767d4fe1
			- https://github.com/fac28/play-dates/blob/73ed1d513efa40118e8a7a9ce22ced9fdf668058/src/routes/home.js#L17-L21
		- I can go to `/form` without being signed in (show how to do protected routes)
		  id:: 651e0022-6c30-455e-9175-407439c3e7a7
			- also form-route.js is not the best naming. it should be more specific to whatever the app is doing (`events.js`)
			- https://github.com/fac28/play-dates/blob/73ed1d513efa40118e8a7a9ce22ced9fdf668058/src/routes/form-route.js#L15-L28
		- similar to above, you can tidy code up by checking for active session straight away and returning early if there isn't one
		  id:: 651e01e0-09ce-43f1-89f7-d299042e611f
			- https://github.com/fac28/play-dates/blob/73ed1d513efa40118e8a7a9ce22ced9fdf668058/src/routes/month.js#L10-L28
## Week 4
- ### TechYEScracy
- Be weary of redundant lines of code and unnecessary logic
```javascript
	router.post("/vote", (req, res) => {
	const user = req.signedCookies ? req.signdCookies.user : false;
	// user is never used 
	// that line could also have been: 
	// const user = req.signedCookies && req.%% signedCokies %%.user

	
	const {poll_id,vote_type} = req.query;
	updatePoll(poll_id, vote_type , 1);
	return res.redirect("../")

});
```
Here's a good chance for a ternary statement:
```javascript
function getPollList(expired) {
if (expired) return select_all_expiredPolls.all();
return select_all_activePolls.all();

// expired ? select_all_expiredPolls.all() : select_all_activePolls.all()
}
```
- Your testing library is a nice set up. Pretty easy to read and the suite you created is fairly comprehensive - barring maybe the description of the actual suite:
```javascript
test("test test", () => { // changing just this would make your logs clearer
assert.equal(1, "1", "Expected 1 to be equal to '1'");
});

test("can create a new user", () => {
reset();

const before = count("users");
createUser("Egg", 20);

const after = count("users");
assert.equal(
	before,
	after - 1,
	"Expected the count of users before to be one less than after creating a new user"
);

});
```
- Version control
	- this repo employs a dev-branch but as a consequence the main branch is actually behind by a few features (even though the dev-branch version is stable) - probably a good idea to review workflows
### Comic-unity
- Consider naming best-practices
	- for example, drawImage() suggests that the function would allow you to draw an image but it's actually returning an HTML template
- Clean up!!
	- If code is commented out by the time you are ready to push then it needs to be removed
```javascript
		// function layout({ title, content }) {
// return /*html*/ `
// <!doctype html>
// <html lang="en">
// <head>
// <meta charset="UTF-8">
// <meta name="viewport" content="width=device-width, initial-scale=1.0">
// <link rel="stylesheet" href="normalize.css">
// <link rel="stylesheet" href="styles.css">
// <title>${title}</title>
// </head>
// <body>
// ${content}
// </div>
// </body>
// </html>
// `;
// }

  

// module.exports = layout;
```
- Here's a nifty change that would have made your code more iterable:
```javascript
const colours = ['black', 'white', 'red', 'orange', 'yellow']

<div class="color-controls">
	colours.map(colour => return {`
		<button id='${colour}-button' class='color-button'></button>
	`})
```
that would get rid of this wall of code:
```javascript
<div class="color-controls">
	<button id='black-button' class="color-button"></button>
	<button id='white-button' class="color-button white"></button>
	<button id='red-button' class="color-button red"></button>
	<button id='orange-button' class="color-button orange"></button>
	<button id='yellow-button' class="color-button yellow"></button>
	<button id='green-button' class="color-button green"></button>
	<button id='blue-button' class="color-button blue"></button>
	<button id='purple-button' class="color-button purple"></button>
</div>
```
and it would allow you to expand the palette available in future by adjusting a simple array.
### ai-art-gallery
- I like your README.md
	- clear and detailed - maybe make it a little more visual (e.g. database schema)
- Nice one, using the github secrets to make your variables available without exposing them
- just a quick props on this here:
```javascript
// in routes/gallery.js
router.get("/", async (req, res) => {

	try {
		const artworkDetails = await selectWork();
		const ids = artworkDetails.map(image => image.id);
		const artworkWithImages = await Promise.all(ids.map(async id => {
		const imageDetails = await displayWorks(id);

		return {
		...artworkDetails.find(artwork => artwork.id === id),
		image_file: imageDetails.image_file,
		};
	}));

return res.send(layout(artworkWithImages));
}
```
	- Using the spread operator here is really slick and your logic is akin to what you'll need when you start managing states soon
## Week 5
### Week5-James_Deepa
- how come you're wrapping these functions within other functions? seems uneccessary (in general it feels like there's too much going on in this component body)
- https://github.com/fac28/Week5-James_Deepa/blob/26152dd0dfae6bddf0e22d9e5e90346081b9613c/src/App.jsx#L32-L43
- move this conditional to be in the parent component rather than in the child component
- https://github.com/fac28/Week5-James_Deepa/blob/26152dd0dfae6bddf0e22d9e5e90346081b9613c/src/components/Gameover.jsx#L4
- https://github.com/fac28/Week5-James_Deepa/blob/26152dd0dfae6bddf0e22d9e5e90346081b9613c/src/components/Win.jsx#L4
- all the files in helpers should probably have `js` extension, and they shouldn't be capitalised (only files that export components should be capitalised)
- it might be better to have a separate hooks directory for hooks
- keytracking should be called `useKeyTracking` as it's a custom hook
### PetProgrammer
- in react, dom properties should be camelCased
- https://github.com/fac28/PetProgrammer/blob/ee7f30426312c1f8c9581606c910c1cbb76d2fe2/src/components/CreateName.jsx#L12
- App.css file name should probably be all lowercase
- this function is a component and should live outside the parent component body
- https://github.com/fac28/PetProgrammer/blob/ee7f30426312c1f8c9581606c910c1cbb76d2fe2/src/App.jsx#L31-L51
- making a prop object like this is not recommended, all properties should be individually spread into objects that need them
- https://github.com/fac28/PetProgrammer/blob/ee7f30426312c1f8c9581606c910c1cbb76d2fe2/src/App.jsx#L26-L29
- you don't need a react fragment here
- https://github.com/fac28/PetProgrammer/blob/ee7f30426312c1f8c9581606c910c1cbb76d2fe2/src/components/Apply.jsx#L21-L25
- this function should have camelCase naming, using uppercase for the first letter is reserved for react components
- https://github.com/fac28/PetProgrammer/blob/ee7f30426312c1f8c9581606c910c1cbb76d2fe2/src/components/Coding.jsx#L12
- why is there a dispatch abstracted away to `isMad`? it seems unnecessary
- https://github.com/fac28/PetProgrammer/blob/ee7f30426312c1f8c9581606c910c1cbb76d2fe2/src/components/Coffee.jsx#L10
### elena-tess-w5
- all your files are inside the subdirectory `myapp` and this could mess around with vscode extension and other things. your readme and package.json should generally live in the top level
- you have two eslint config files, you should get rid of one of them
- you don't have prettier set up
- using a lot of ternary operators within in the markup makes the code confusing to read, I would consider refactoring this
- https://github.com/fac28/elena-tess-w5/blob/e15af0ea3f255d5f9248f496e997a75876687af5/myapp/src/components/TriviaApp.jsx#L59-L106
- the reset button has a onClick handler called `incrementCount`, it should probably have a better name
- https://github.com/fac28/elena-tess-w5/blob/e15af0ea3f255d5f9248f496e997a75876687af5/myapp/src/components/TriviaApp.jsx#L101
- i'm pretty sure nowadays you don't need react
- https://github.com/fac28/elena-tess-w5/blob/e15af0ea3f255d5f9248f496e997a75876687af5/myapp/src/components/QuestionNavigation.jsx#L1

### react-minesweeper-dylan-george
- lots of variables defined but not used [here](https://github.com/fac28/react-minesweeper-dylan-george/blob/bddd49e738d2bee0a6ab6a99acf07233414f4786/src/components/Modal.jsx#L1-L28)
- no instructions for how to run the project in readme
- you have a few [gameState states](https://github.com/fac28/react-minesweeper-dylan-george/blob/bddd49e738d2bee0a6ab6a99acf07233414f4786/src/App.jsx#L9), they should live in constants so that you reduce the chance of making mistakes and so you can easily know what all the possible states are
- there's no need for a react fragment [here](https://github.com/fac28/react-minesweeper-dylan-george/blob/bddd49e738d2bee0a6ab6a99acf07233414f4786/src/components/Board.jsx#L6-L22)
- good candidate for a [switch statement](https://github.com/fac28/react-minesweeper-dylan-george/blob/bddd49e738d2bee0a6ab6a99acf07233414f4786/src/components/Cell.jsx#L21-L30) (but more of stylistic preference rather than anything else)
- you have both and index.css and an App.css and one of them is empty
### sound-control
- because your state is quite complex, i would consider using `useReducer` rather than `useState`
- [`compareArrays`](https://github.com/fac28/sound-control/blob/26843bb9928af90864ffc656a738e227fec64755/src/utils/compareArrays.js#L2-L15) could have better naming, you're checking for equality rather than just comparing so something along those lines
- [nested ifs](https://github.com/fac28/sound-control/blob/26843bb9928af90864ffc656a738e227fec64755/src/components/Pad.jsx#L16-L29) and else could look cleaner by employing early return
- play button and reset button are the same, do they need to be separate components?
- do they even need to be abstracted out from App.jsx?
- [here](https://github.com/fac28/sound-control/blob/26843bb9928af90864ffc656a738e227fec64755/src/App.jsx#L35-L42) you can use && instead of using ternary operator
### battleship
- no instructions for how to run app in readme
- eslint not set up properly
- lots of console.logs left in
- the surrounding div [here](https://github.com/fac28/battleship/blob/05e5ee6fba69f5bd148c5e468eb17e5e648467ec/src/components/Game.jsx#L33-L38) could just be a fragment
- [this](https://github.com/fac28/battleship/blob/05e5ee6fba69f5bd148c5e468eb17e5e648467ec/src/components/ComputerBoard.jsx#L35-L41) should live in a `useEffect`, (come and ask me if it doesn't make sense why)
- is there any advantage to abstracting [this button](https://github.com/fac28/battleship/blob/05e5ee6fba69f5bd148c5e468eb17e5e648467ec/src/components/PlaceShipsButton.jsx#L1-L8) to a different file?
- there's an empty `index.js` file which you should remove from the codebase
