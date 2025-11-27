🛠️ The Chore Checker Build
📜 HTML & Structure (The Skeleton)
The HTML is the most straightforward part—it just sets up the boxes and text.

Header: Greets you with "Hey there! 👋" and a funny little waving emoji that actually wiggles (that's the CSS magic!). It sets the casual, friendly tone.

The Main Box (.box): This is the core element. It's a nice, clean white box with rounded corners and a slight shadow to make it look like a floating card. And yeah, I added an animation to make the whole box gently bob up and down (@keyframes floaty)—because why should a chore list be boring?

Chore Display: This is the container (.chore-display) where the daily assignments show up. It uses a clean, light blue background (#eef0ff) to clearly separate it from the main box.

Footer: My own little gamer-geek sign-off, powered by snacks! 🎮

🎨 CSS & Style (The Aesthetics & Animation)
I kept the CSS simple but cute. I'm using a clean sans-serif font (Poppins—it's great!) and a soft blue/white color scheme (#fafaff and #fff).

Layout: I used display: flex on the body to center everything vertically and horizontally. This is way easier than fighting with margins.

Animations: This is the fun part!

Wiggle (@keyframes wiggle): The waving hand emoji (👋) rotates quickly back and forth to make it look like it's actually waving. This is a classic little touch!

Floaty (@keyframes floaty): The entire .box moves -6px up and down infinitely. It makes the checklist feel light and playful, not like a heavy, boring list of tasks.

Chore Rows: I used Flexbox again (display: flex with justify-content: space-between) on the .row elements to perfectly space the chore name and the person assigned to it (if I had added that later, but right now it just spaces the text).

💻 JavaScript & Logic (The Brains)
This is where I put my coding energy! The JavaScript is the whole reason the chores rotate automatically every day.

The Chore Rotation Hack: Instead of using a complicated server or database (which is overkill for a simple list), I used the current date to decide who does what.

getDayIndex(date): This function calculates the number of days that have passed since January 1, 1970 (the "epoch," which is what computers use).

idx = getDayIndex(today) % chores.length: This is the key formula. I take the total number of days and use the modulus operator (%) with the number of chores (which is 2). The result will only ever be 0 or 1.

Assignment:

Muhsina (Person 1) gets the chore at index idx (either 0 or 1).

Maher (Person 2) gets the other chore, which is calculated using (idx + 1) % chores.length.

The Result: Since the day index changes exactly once every 24 hours, the idx alternates between 0 and 1 every single day, which means the chores (Sweeping vs. Washing) automatically swap between me and Maher! Perfect rotation, no arguments needed! 😈

It's a tiny, fun project that gets a job done and shows off some slick CSS animations and simple, effective JavaScript logic!
