# Flow 1 coded prototype: changes since the first version

The first version was delivered on Oct 30 at 7:36 pm. These are the changes you asked for since then, in order. Everything is in [flow-1-prototype.html](/mnt/project-files/flow1-prototype/flow-1-prototype.html).

## 1. Pinterest brand alignment (Gestalt)
- Every margin, gap and padding now follows Pinterest's 4px spacing scale.
- Buttons come in 48, 40 and 32px heights, with 16, 12 and 8px rounding. Icon buttons are circles.
- Chips and the status pill are 40px tall with 12px rounding.
- Text fields are 48px tall, with 1px borders, 16px rounding and Pinterest's blue focus ring.
- Type sizes, colors (including disabled and error states) and shadows use Gestalt's values in light and dark mode.

## 2. Editable project dates
- On New project and on the project page, click a date on the calendar to set the start, then click again to set the finish.
- Arrows move between months.
- The timeframe chip switches to Custom when the dates don't match a preset.
- On the project page, changing the dates shows a toast and is logged in Activity.

## 3. Pinterest hover, click and scroll behavior
- **Hovering a pin:** a dark wash appears with a board picker, a red Save button, the source link, and share and more buttons.
- **Hovering anything else:** colors fade over 300ms.
- **Clicking:** pins and cards shrink to 97% while pressed. Picking a board from the menu saves the pin to that board.
- **Feed layout:** a masonry grid with color placeholders while images load. More pins load with skeletons as you scroll.
- **Going back:** you return to the same spot in the feed.
- **Close-up:** the action bar stays pinned at the top.
- **Mobile:** the tab bar and chip bar hide when you scroll down.

## 4. Sidebar selected and hover states
- **Selected:** the current page shows a filled black icon instead of a black tile.
- **Hover:** a light rounded square appears behind the icon, then a black tooltip shows the item's name.
- **Notification dots:** Explore and Notifications have red dots.
- **Icons:** I redrew home, board, create, messages and customize to match Pinterest's set.

## 5. Spacing pass on every screen
- Sections are 32px apart on desktop and 24px on mobile.
- Headings sit 16px above their content, labels sit 8px above their fields, and list rows are 40px tall.
- **Notifications** moved up, right under the calendars, on New project and on the project page.
- I also fixed these layout problems:
  - The Add step tile had wrapped onto its own row.
  - The ideas search bar was squashed.
  - The mobile filter chips were cut off.

## 6. Saved boards page and board page
- The Saved icon opens a new Boards page.
  - It has Pins, Boards and Collages tabs, filter chips, a + button and six board cards.
  - Each card has a large cover, a title, the pin count and when the board was last updated.
- Clicking a card opens the board, laid out like your Fashion outfits screenshot:
  - Title with the "Public board · N Pins" line.
  - Avatars with an add-collaborator button.
  - Organize, More ideas, Shop, Collage and Project tiles.
  - An outlined "Search this board" field with a filter icon.
  - A floating + button.
- The top search reads "Search your Pins" and has a mic icon.
- The mobile board page uses the same layout.

## 7. Project straight from a board
- Project on a board opens the project builder directly.
- The builder opens with a split collage cover made from the board's images.
- The ideas panel opens on Your boards, with that board already selected.
- Steps are labeled "Suggested from your board".

## 8. Profile pictures
- June's photo appears in the top bar, on her profile, in the collaborator lists and in the comment boxes.
- Ruth's and Priya's photos appear on their comments. Ruth's also shows in the collaborators row.

## 9. Projects and Boards pages
- I removed Season recap from the Projects page.
- I added a Projects tab next to Collages on the Boards page.

## 10. Match to the Figma screens (where they differed, pinterest.com won)
- **Home feed:**
  - The filter chips are now text tabs with an underline.
  - On mobile, there's a top bar with the logo, a + button and June's avatar.
- **Create on desktop:** a full-height panel docked beside the sidebar, with Project highlighted and a black New badge.
- **Create sheet on mobile:** bigger tiles, a black Project tile and a left-aligned title.
- **Pin close-up:**
  - Back, expand and visual search buttons sit on the image.
  - A board picker sits next to Save.
  - Visit site is full width.
  - The comments header has a chevron.
  - The comment box has emoji and photo buttons.
  - The sparkle is gone from Make this.
- **Page titles:** bigger on New project, the project page and Made it. On Made it, the badge sits under the title.
- **New project:** Change cover is a text link, and the ideas panel has a divider on its left.
- **Mobile Projects:** June's avatar sits next to left-aligned tabs, and the search box has an outline.
- **Mobile photo detail:** the background is white instead of black.

## 11. Completing a project early
- June can't complete a project while steps are still open. The old "Complete anyway" option is gone.
- Tapping Complete project early shows a gentle message: "You have 3 steps left. Finish them to complete this project. Your project is saved as in progress, so you can pick up right where you left off."
- The Keep it in progress button closes the message and shows a "Saved as in progress" toast.

## 12. A more readable and accessible message
- **Easier to read:**
  - White card with a dark outline and a thick bar on its left edge.
  - A larger bold title.
  - Full-black body text at a bigger size.
  - The alert icon sits in a circle.
  - The button is at least 44px tall.
- **Accessible:**
  - When the message appears, the page scrolls to it and moves focus there, and screen readers read it out.
  - Complete project is marked unavailable and explains why.
  - With reduced motion turned on, the scroll and fade-in are skipped.

## 13. A red accent on the message
- The outline and the thick left bar are now red, and the card has a light red tint.
- The title and the alert icon are dark red, and the icon sits in a pale red circle.
- The body text stays black, and every colour passes WCAG AA contrast in light and dark mode.

## 14. A movable roadmap and a dark mode pass
- **Roadmap columns:** To start, In progress and Complete no longer show counts.
- **Moving steps:** drag a step card to another column, or use its ⋯ button to pick a column. The ⋯ button works by keyboard and on touch.
  - Several steps can be in progress at the same time.
  - Steps are completed in order. If June tries to complete a step early, the Complete column outlines in red and a message says which step to finish first.
  - Completed steps reopen from the latest one back, so the order always stays true.
  - Each move is logged in Activity and confirmed with a toast.
- **Step list:** Mark done shows only on the next step in order. Other open steps get Start this step or Move back to To start, with a note saying when they can be marked done.
- **Dark mode:**
  - Secondary text is lighter.
  - Grey panels, such as the roadmap columns, the next step card and tags, are darker.
  - Borders are a little brighter.
  - Every text element on all 21 screens now passes WCAG AA contrast in dark mode.

## 15. Choose a Pin on a blank project
- When you start a blank project, the cover no longer shows an empty image icon. A red Choose a Pin button sits on the grey cover placeholder instead.
- On desktop, the button opens a "Pick a Pin to start from" dialog with More ideas, Your boards and Brand kit. On mobile, it opens the same picker as a sheet.
- Picking a Pin fills in the title, cover and suggested steps. Change cover shows only once there's a cover.

## 16. Quieter mobile confirmations and a Pinterest-style Mark done
- **Mobile:** marking a step done no longer pops up a toast that covers the next step. A quiet "Step 3 done · Undo" line appears under the finished step instead, and screen readers announce it. Desktop keeps its toast.
- **Mark done:** it's now Pinterest's red primary button, without the check icon, and it comes first in the row. On mobile it's full width and 48px tall, with Ask about this step and Edit below it. Before, it was a black button that wrapped onto its own line under the secondary buttons.

## 17. A Pinterest-style "steps left" message
- The message now follows Gestalt's slim error banner: a soft red background, rounded corners, a filled red alert icon and one line of text. The white card, border and left stripe are gone.
- New copy: "**You have 3 steps left.** Mark them done to complete this project."
- Removed the Keep it in progress button. The message just explains why the project can't be completed yet.
- The message goes away by itself once every step is done, and Complete project works again.
- Dark mode uses a deep red background with light text, and both modes pass AA contrast.

## 18. Fixes from testing
- **Create project:** the button that creates a project now says Create project instead of Next, on desktop and mobile.
- **Make this tooltip:** hovering or focusing Make this on desktop shows "Turn this Pin into a project with steps". On mobile, screen readers hear the same line.
- **The next step lives in its card:** the next step card now shows the step's instructions, Mark done and Ask about this step, so nobody has to scroll down to the step list. After Mark done, the card moves on to the next step. On mobile, a quiet "Step N done · Undo" line appears at the top of the card.
- **Mobile opens on Steps:** a new project on mobile opens on its roadmap and steps, with Steps and Overview tabs at the top. Opening a project from the hub works the same way.
- **Pick your Pins:** Project on a board now starts with a pick-your-Pins step. The first 6 Pins are selected, and you can change them before you continue. The new project's title is filled in with the board name. This works on desktop and mobile.
- **References with sources:** references now show a thumbnail, the Pin's name and its source site, like kilnandco.com. Videos and PDFs show an icon and the source of the Pin they came from. This applies on the create form and the project page.

## 19. A simpler project page
- **Taller cover:** the project image at the top right is now a 2:3 vertical rectangle, the shape of a Pin.
- **Next step moves forward on its own:** when a step is marked done and moves to Complete, the next step moves into In progress on the roadmap.
- **No more Steps section:** the list of step dropdowns under the roadmap is gone, since it repeated the roadmap. Its tools now live in the top step card: instructions, the video link, Upload work, Ask about this step and Mark done.
- **Roadmap cards open in the step card:** clicking a step on the roadmap shows that step in the top card. Done steps get Mark not done (on the latest one), and later steps get Start this step. "Back to next step" returns to the next step.
- **Save progress:** the full-width button under Materials says Save progress until every step is done. Then it becomes Complete project. Since you can't complete a project early anymore, the "steps left" message no longer appears.
- **Step card style:** the top card now matches the step dropdowns: a white card with a border, the step's status badge and label in a header row, and the time estimate on the right of that row. The image, copy and buttons stay where they were.

## 20. Task card polish and a spacing pass
- **New time icon:** the time estimate in the task card header uses an hourglass instead of a clock, so it no longer repeats the clock in the In progress badge.
- **Vertical task image:** the step image in the task card is now a 2:3 vertical rectangle, like a Pin. On desktop it's 160px wide beside the step. On mobile it's 96px wide beside the step title, with the instructions and buttons full width below.
- **Spacing on Gestalt's 4px scale:** the task card has 24px padding on desktop and 16px on mobile. Sections sit 32px apart on desktop and 24px apart on mobile. The roadmap hint sits 8px under the roadmap, and Materials has the same 16px title gap as the other sections. On mobile, the task card starts 16px under the Steps and Overview tabs instead of 8px.

## 21. Calendar under Materials, and autosave
- **Calendar moved:** the project calendar now sits under Materials in the main column, on desktop and on the mobile Steps tab. It's no longer in the side panel or on mobile Overview. On desktop, the months sit side by side.
- **Only the months you need:** calendars show only the months a project's dates cover, up to three. A project inside one month shows one month, and one from Oct 26 to Nov 8 shows two. The arrows still move to earlier or later months. This applies everywhere, including the create form.
- **Autosave:** Save progress and the Save button in the project header are gone. Every change saves as it happens, and a quiet "✓ Saved" status sits in the header. Complete project still appears once every step is done.

## 22. Boards icon, nav hovers and a smaller overview image
- **Boards icon:** the boards icon in the side nav now matches pinterest.com. When it isn't selected, it's an outlined rounded square split into one tall panel and two stacked panels. When it's selected, the same shape is filled black with white gaps. Its tooltip now says "Your boards".
- **Nav hover, for every side nav icon and the logo:** a very light grey (#FAFAF9) 48px tile with 16px corners appears behind the icon. A black tooltip with 12px corners appears 12px to the right, with white 13px text and no shadow. In dark mode, the tile is dark grey and the tooltip is white with black text.
- **Smaller overview image:** on the desktop project page, the cover in the Overview panel is now 240px wide, still at 2:3.

## 23. Calmer step card icons
- The "Next step" badge on the project progress page now uses a half-filled circle (in progress) instead of a clock.
- The time estimate in the card header is plain text; the sand timer icon is gone.

## 24. Pick your Pins comes first
- Every project that isn't started from a Pin now opens on a "Pick your Pins" step (Step 1 of 2) before the project form. This covers the Create menu on desktop, the Create sheet on mobile, and the Projects hub (Create menu, New project card and the empty state).
- You can browse your boards or More ideas, select one or more Pins, then press Next. The first Pin fills the title and steps; the others become the cover and references.
- "Start without a Pin" stays as a quiet text link for people with no Pin in mind.
- Starting from a Pin close-up still skips this step, and the board path keeps its own Pin selection.
- New jump points: D5p and M7 "Pick your Pins".

## 25. Calendar months keep one size
- Every calendar month keeps the size it has in the two-month layout, on the New project form and the project page.
- 1 month: same size, with white space beside it.
- 3 to 4 months: they wrap into a two-column grid at that size.
- 5 months or more (up to 12): the months become a sideways-scrolling gallery that snaps to each month, with the note "Scroll sideways to see all N months".
- On mobile, months stack full width up to 4, then switch to the same gallery.
- After you pick a finish date, the calendar goes back to the start month so the whole plan reads from the beginning.

## 26. Calendar arrows and date pickers
- When the months stack vertically (3 to 4 months on desktop, 2 to 4 on mobile), a round down-arrow button reading "See all N months" sits under the first row. It nudges twice, or not at all with reduced motion, and clicking it scrolls to the next row.
- In the sideways gallery (5+ months), "Scroll sideways to see all N months" is now a button that moves the gallery one month.
- Start date and End date pickers sit above the calendar on the New project form and the project page. They use the native date picker and stay in sync with the calendar both ways.
- Moving the start past the end shifts the end to keep the plan length, and the end can't be set before the start.
- Changes on the project page are logged and confirmed with a toast, the same as calendar clicks.
- Help copy now reads "Or click a start date, then an end date, on the calendar."

## 27. Bigger scroll arrow beside the calendars
- The scroll arrow is now a 56px black round button in a rail to the right of the calendars. It is 48px on mobile.
- It stays in view while you scroll past the months, and it nudges three times, or not at all with reduced motion.
- When months stack vertically it points down. Each click scrolls to the next month below, and after the last one it returns to the first.
- In the 5+ month gallery it points right and moves one month sideways. The "Scroll sideways" note stays under the gallery.
- The rail space is always reserved, so every month keeps the same size whether there are 1, 2, 4 or 6 months. On desktop the Start and End date fields line up with the calendar columns.

## 28. Centred arrow and Pinterest-style date pickers
- The calendar scroll arrow stays on the right and now sits at the vertical midpoint of the calendars instead of following the scroll.
- Start date and End date are now Pinterest-style fields: a 16px-rounded field that shows "Oct 26, 2026" with a calendar icon.
- Each field opens a white popover with a soft shadow: month arrows, a weekday row, round 40px day buttons, a black selected day, a ringed "today" and grey days inside the plan. End dates before the start are greyed out.
- Picking a day updates the calendar and closes the popover, then focus returns to the field. Escape or a click outside also closes it.
- The native browser date picker is gone.

## 29. Project steps under the roadmap
- The project progress page shows a "Project steps" section under the Roadmap on desktop and mobile, matching the reference.
- Its heading carries a grey "Suggested from the Pin's tutorial" chip, or "Suggested from your board" for board projects.
- Each step is a rounded landscape photo with "Step N" in grey and the step title in bold underneath. Desktop shows 5 per row, mobile 2.
- A dashed "+ Add step" tile adds a step inline and confirms with a toast.
- Clicking a step opens it in the top step card.

## 30. Brand pass and profile photos
- Pin close-up, desktop: the board picker and Save now sit in the top action bar beside the icons, like Pinterest. The board name is cut off with an ellipsis when it's too long.
- Pin close-up, desktop and mobile: Make this moved below into its own card, "Turn it into a project · Get steps, materials and a plan from this Pin", with a Make this button.
- Every avatar now has a real profile photo. Hello Stitch Studio has a maker portrait. Other creator accounts use a photo from one of their own Pins. Invited collaborators get one of three new portraits.
- Spacing is on the Gestalt 4px scale everywhere: 24 leftover 6px gaps and paddings are now 8px or 4px. These cover tags, badges, labels, the tab bar, the Create sheet, category tabs, Pin overlays, step tiles, the lightbox and menus.
- Type is on the Gestalt scale only: 12, 14, 16, 20, 28 and 36px. Tooltips went from 13px to 12px, and lightbox captions from 11.7px to 12px.
- Mobile touch targets: comment Reply and Like, text links and lightbox dots are now at least 24 to 32px tall.
- Button sizes were checked and stay consistent: 48px with 16px corners, and 40px with 12px corners.

## 31. Make this button with hover tip

- On the Pin close-up, Make this is now a single secondary button right-aligned under Save (desktop and mobile).
- "Turn this into a project" appears as a black tooltip beside the button on hover or keyboard focus.

## 32. Check-in days bordered in black

- Check-in days on every calendar now have a Pinterest black border instead of red, and the legend swatch matches.

## 33. Mobile progress page matches desktop; Make this without icon

- Mobile Steps tab: status dropdown and Saved now sit at the top like desktop.
- Mobile task card: wide horizontal image on top, then title, steps, links, and Mark done and Ask about this step side by side.
- Mobile Project steps: one horizontal row of step images you swipe through, like the desktop row.
- Make this button no longer has an icon.

## 34. Make this under the Pin title

- On the Pin close-up (desktop and mobile), Make this now sits directly under the Pin title, aligned left. The hover tip appears to its right.

## 35. Mobile Make this beside Save

- On the mobile Pin close-up, Make this now sits inline to the left of Save. The tip shows above it on focus.

## 36. Mobile creator row under the title

- On the mobile Pin close-up, the studio name and Visit site now sit under the Pin title.

## 37. Mobile progress page: calendars in a row, overview sections; step references in task cards

- Mobile progress page: all the plan months sit in one swipeable row with the next month peeking in. No arrow.
- Mobile progress page: Overview, Activity and Files, with Visibility, Notifications, References and Collaborators, now follow the calendar.
- Desktop and mobile: each task card shows the references for that step above Upload work (for example, the chain stitch video on Step 3 and the pattern PDF on Steps 1 and 2). This applies to the expanded step cards too.

## 38. Pin info layout from the reference

- Pin close-up info (desktop and mobile): a small avatar with the creator name in caps, then a large bold title, a Description heading, grey text cut off after three lines, and a right-aligned See more that expands it.
- Desktop: Make this sits under the title, and a full-width Visit site sits under the description.
- Mobile: Make this stays beside Save, and a full-width Visit site sits under the title.
- The old site link, the Follow row and the separate creator row were removed.

## 39. Brand review pass

- The creator name on the Pin card is no longer all caps.
- The last off-grid spacing (6px on the lightbox caption) is now 8px.
- Lightbox dots and short category tabs now have at least a 32px tap area.
- Audit across all 22 screens: spacing on the 4px grid, radii on the scale, type only from the brand scale (12/14/16/20/28/36, plus 24 for the mobile Pin title from the reference), button heights 40/48, and every mobile tap target at least 32px.

## 40. Mobile Pin info order, comment bar, all-done card

- Mobile Pin card: creator, then title, then Description, then a full-width Visit site under the description, as on desktop.
- Comment bar (desktop and mobile): a white pill with a light grey outline, 16px text, a readable placeholder and icons that fit inside. It no longer runs off the screen on mobile.
- The "All 5 steps done" card now uses the same card style as the step cards: header with a check, the project image, title, text and Complete project.

## 41. Upload on the all-done card, no Change cover

- The "All 5 steps done" card has "Upload project photos and files" (photos, videos or PDFs, several at once). Uploads show in the card, appear in the Files tab, and are logged in Activity.
- Removed "Change cover" from the new project planning page (desktop and mobile).

## 42. Mobile New project calendars stack

- On the mobile New project page, every month of the plan now stacks vertically at full width, however long the plan is. There is no scroll arrow and no sideways gallery.

## 43. Mobile New project calendars swipe

- Replaces 42: on the mobile New project page, the months sit in one swipeable row with the next month peeking in, the same as the mobile progress page. No arrow.

## 44. Calendars follow today

- The prototype uses the real date. New projects start today with a 2-week plan. The sample stamps project and its done dates shift so they always sit around the current month.
- On a new project (desktop and mobile), past days and months cannot be picked. The previous-month arrows stop at this month.
- Picking a start date in a later month, on the calendar or in the Start date picker, makes that month the first one shown. While choosing an end date, the next month stays in view too.

## 45. Accessibility and legibility pass
- Search bars: placeholder text now passes WCAG AA in light and dark (it was falling back to the browser grey, 2.2:1 in dark mode). Typed text is 16px in Pinterest black/white, search icons are full-strength, every search field has a label, and focus shows the Gestalt blue ring.
- All placeholders (forms, comments, replies) use the same readable grey.
- Pins can be opened from the keyboard with a visible focus ring, without nesting buttons inside buttons.
- Create menu, calendar month headings and board tabs fixed for screen readers and focus rings.
- axe-core scan of 22 screens in light and dark: 0 violations.

## 46. Responsive desktop and mobile
- Checked every screen from 320px phones up to 2560px monitors. No sideways scrolling at any width.
- Tablet widths (760 to 900px): the Pin close-up keeps the image and details side by side, and the New project cover and Made it photo stay a sensible size beside their content instead of filling the screen.
- Wide monitors: the New project and progress pages and the Made it page are centered with a max width instead of hugging the left edge. Made it photos fill more columns as the screen grows.
- Small phones (under 360px): the task card buttons stack so "Ask about this step" isn't cut off.

## 47. Desktop spans the full screen
- Removed every width cap on desktop pages (Pin close-up, Pick your Pins, New project, progress, Made it). Content now runs edge to edge with the same 24px gutter as the home feed, with no empty side margins.
- Side columns (ideas panel, project overview) and the Made it cover grow with the screen. Project cards and Made it photos add columns as the screen widens.
- Still responsive down to tablet widths, and below about 760px it switches to the mobile layout.

## 48. Pin page matches Pinterest's close-up
- The Pin card is Pinterest's centered close-up again: 1016px max, 32px corners, soft shadow, image on the left at its natural ratio, details on the right with the sticky action bar.
- The back arrow sits outside the card on the left, the way Pinterest places it.
- "More to explore" is centered and the feed below runs the full width of the screen.
- Under about 1000px the card stacks into one 508px column (image on top), with the back arrow on the image, like Pinterest.

## 49. Desktop page layouts match Celeste's reference screens
- Pin page: the Pin card spans the feed (all columns but one), with a column of Pins running beside it on the right and the feed continuing underneath, as on Pinterest. The image fills the left half of the card, with the back arrow on it. Narrower windows (under 4 feed columns) drop the side column.
- New project and project page: the ideas panel and the Overview panel sit full height against the right edge, behind a divider, and stay put while the left column scrolls. The header sits over the left column only. The project cover in Overview is landscape.
- Made it: a photo collage up top (finished photo plus two step photos) beside the description; step photos are tall and run five across the full width; "More to explore" is left-aligned.
- Buttons and text unchanged. Desktop only.

## 50. Desktop task cards in Pinterest's close-up style
- The progress page task card (and the "All steps done" card) now looks like a mini Pin close-up: no border, 32px corners, Pinterest's soft shadow, and the step photo filling the full height of the left side like a Pin.
- Step title is the Pin title size; instructions are 16px; buttons are full 48px pills.
- Dark mode uses a hairline outline instead of the shadow. Under 900px the photo sits on top at 16:9.

## 51. Tall first collage photo, tablet layouts restored
- Made it (desktop): the first of the three collage photos is now a tall vertical rectangle, with the two step photos stacked beside it.
- Tablet widths (760 to 1199px) use the earlier responsive layouts again: the centered Pin close-up card, the New project and project pages without the edge-to-edge side panel, and the single Made it photo. The layout switches live when the window is resized.
- Desktop (1200px and up) and mobile stay exactly as they were.
