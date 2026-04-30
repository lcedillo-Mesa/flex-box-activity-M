# Lens & Light — Photography Blog
### CSS Flexbox Activity

You have been given an `index.html` and a `style.css` file. The HTML is complete — do not change it. Your job is to fill in the missing CSS values so your page matches the mock-up.

---

## Resources

- **Flexbox cheat sheet** — your printed reference sheet
- **CSS-Tricks flexbox guide** — https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- **Mock-up** — the reference image showing what your finished page should look like

---

## Word Bank

You will use these values throughout the activity.
Each one is used at least once — some more than once.

```
flex        row        column        flex-start
flex-end    center     space-around  1
```

---

## Before You Start

Open these three things side by side in Codespaces:

1. `style.css` on the left
2. The live preview (right-click `index.html` → Open with Live Server)
3. The mock-up reference sheet

Save with **Ctrl + S** after every change and check your preview before moving on.

---

## Step 1 — Header

**Goal:** Title and tagline stack top to bottom. Text sits on the **left** side.

Find `.header` in your CSS. You will see two properties with the wrong values — the comments in the file tell you which ones.

**Change 1 — flex-direction**

Right now items go left to right. You need them to go top to bottom.

Which value makes items stack top to bottom?

```css
flex-direction: ???;
```

> **Hint:** Think about columns in a table — they go up and down.

**Change 2 — justify-content**

Right now items are pushed to the right. You need them on the left.

Which value puts items at the start?

```css
justify-content: ???;
```

> **Hint:** The start of a row is the left side.

**Save and check your preview.**

✅ Does the header text sit on the left? If yes move to Step 2.

---

## Step 2 — Nav

**Goal:** Links sit **side by side** with space evenly around each one.

Find `.nav` in your CSS. There are two things to fix.

**Change 1 — flex-direction**

Right now items stack top to bottom. You need them side by side.

Which value makes items go left to right?

```css
flex-direction: ???;
```

> **Hint:** Think about rows in a table — they go across.

**Change 2 — justify-content**

This line is commented out in the file. Remove the `/*` and `*/` around it to turn it on:

```css
/* justify-content: space-around; */
```

becomes:

```css
justify-content: space-around;
```

**Save and check your preview.**

✅ Are the links side by side with even spacing? If yes move to Step 3.

---

## Step 3 — Hero

**Goal:** Title and text sit **side by side**.

Find `.hero` in your CSS. There are two things to change.

**Change 1 — flex-direction**

Update the value from `column` to `row`:

```css
flex-direction: ???;
```

**Change 2 — align-items**

Remove this line completely — it is not needed when items are in a row:

```css
align-items: center;
```

**Save and check your preview.**

✅ Are the title and text sitting next to each other? If yes move to Step 4.

---

## Step 4 — Main

**Goal:** Sidebar and images sit **side by side**.

Find `.main` in your CSS. Two things are missing — the comments in the file tell you where to add them.

**Add line 1 — display**

Type this on the first line inside `.main { }`:

```css
display: flex;
```

**Add line 2 — flex-direction**

Type this on the next line:

```css
flex-direction: ???;
```

Which value makes the sidebar and images go side by side?

> **Hint:** Side by side means left to right.

**Save and check your preview.**

✅ Is the sidebar sitting next to the images? If yes move to Step 5.

---

## Step 5 — Sidebar

**Goal:** Photo info stacks **top to bottom**.

Find `.sidebar` in your CSS. One value needs to change.

Right now items go left to right. Change the value so they stack top to bottom.

```css
flex-direction: ???;
```

> **Hint:** You used this value in Step 1.

**Save and check your preview.**

✅ Is the camera info stacking vertically? If yes move to Step 6.

---

## Step 6 — Images

**Goal:** Two photos stack **top to bottom** and fill the space equally.

Find `.images` in your CSS.

**Change 1 — flex-direction**

Change the value so the photos stack:

```css
flex-direction: ???;
```

Find `.photo` in your CSS.

**Change 2 — flex**

The value is `0`. Change it so both photos share the space equally:

```css
flex: ???;
```

> **Hint:** Look at the word bank — which number makes items share space equally?

**Save and check your preview.**

✅ Are both photos stacked and the same height? If yes move to Step 7.

---

## Step 7 — Footer

**Goal:** Footer content sits on the **left** side.

Find `.footer` in your CSS. Change the value of `justify-content` so the content moves to the left:

```css
justify-content: ???;
```

> **Hint:** The left side is the start of a row.

**Save and check your preview.**

✅ Is the footer text on the left?

---

## You Did It!

Your page should now match the mock-up. Go through this checklist:

- [ ] Header text is on the left
- [ ] Nav links are side by side with even spacing
- [ ] Hero title and text are side by side
- [ ] Sidebar and images are side by side
- [ ] Sidebar info stacks top to bottom
- [ ] Two photos stack top to bottom and are the same height
- [ ] Footer content is on the left

If anything does not match, go back to that step and re-read the hint.

---

## Bonus — Fun Surprises

Try these one at a time. Undo with **Ctrl + Z** if you want to go back.

- In `.body` change `flex-direction: column` to `flex-direction: column-reverse` — what happens?
- In `.nav` change `space-around` to `space-between` — what changes?
- In `.header` change `flex-direction` back to `row` — what happens to the title and tagline?

Write down what you notice before you undo.

---

## Bonus — Responsive Font Sizes

All font sizes in the file use `px` which is a fixed unit. Try updating some to `rem` instead.

| px | rem |
|----|-----|
| 11px | 0.7rem |
| 12px | 0.75rem |
| 13px | 0.85rem |
| 14px | 0.9rem |
| 18px | 1.125rem |
| 22px | 1.375rem |

Refresh the page after each change to see the effect.

---

## Challenges

You have finished the main layout — great work! The HTML is written for you below. Copy and paste it into `index.html` in the place described, then complete the CSS in `style.css`.

---

### Challenge 1 — Gallery Section

Add a row of photo cards that wraps to the next line when there is no room.

**Step 1** — Copy this HTML and paste it after the closing `</div>` of `.main` in `index.html`:

```html
<div class="gallery">
  <div class="gallery-heading">Gallery</div>
  <div class="gallery-grid">
    <div class="gallery-card">Photo 1</div>
    <div class="gallery-card">Photo 2</div>
    <div class="gallery-card">Photo 3</div>
    <div class="gallery-card">Photo 4</div>
    <div class="gallery-card">Photo 5</div>
    <div class="gallery-card">Photo 6</div>
  </div>
</div>
```

**Step 2** — Find `.gallery-grid` in your CSS and fill in the four `???` values:

- `display` — what turns flexbox on?
- `flex-wrap` — which value lets items move to the next line? (not `nowrap`)
- `gap` — pick a value like `12px` or `16px`
- `justify-content` — how do you want the cards spaced?

> **Hint:** Look at your cheat sheet under `flex-wrap`.

✅ Do the six cards appear in rows and wrap when the window is narrow?

---

### Challenge 2 — About Me Section

Add a section with a profile photo on the left and your bio on the right.

**Step 1** — Copy this HTML and paste it after the `.gallery` div in `index.html`:

```html
<div class="about">
  <div class="about-image">Photo</div>
  <div class="about-content">
    <div class="about-name">Your Name</div>
    <div class="about-bio">Write a short bio about yourself here.</div>
    <div class="about-tags">
      <div class="about-tag">Portrait</div>
      <div class="about-tag">Street</div>
      <div class="about-tag">Golden Hour</div>
    </div>
  </div>
</div>
```

**Step 2** — Find `.about`, `.about-content`, and `.about-tags` in your CSS and fill in the `???` values.

Answer these questions first:

- Should `.about` have the image and text side by side or stacked?
- Should `.about-content` have the name, bio, and tags stacked or in a row?
- Should `.about-tags` have the tags side by side?

> **Hint:** You will use both `row` and `column` — look at the mock-up carefully for each one.

✅ Is the image on the left with your bio next to it? Are the tags in a row?

---

### Challenge 3 — Your Own Section

Design and build your own section. You choose everything.

**Step 1** — Decide what your section will show:
- A contact row with your name and email side by side
- A centred quote from a photographer you admire
- A stats row — photos taken, locations visited, years shooting

**Step 2** — Add your HTML to `index.html` with your own class names.

**Step 3** — Write the CSS at the bottom of `style.css`. Use at least **two flex properties**.

> **Tip:** Start with `display: flex` on the parent. Add one property at a time and save after each one.
