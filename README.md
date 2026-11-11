# Form builder with AI

Interactive prototype of a unified form builder with AI generation. Describe a form to Thryv AI, answer two quick questions, watch it build, then style, refine and publish it in the same builder used for forms built by hand.

Built from the Figma design on demo data, as a companion to the Form Unification case study at [dbyxdesign.com](https://dbyxdesign.com/case-form-unification.html).

## One prototype, every way in

Everything is clickable, and every path lands in the same builder.

**Create with AI.** Thryv AI opens in a new tab. Pick one of the commonly created forms or describe your own, answer two questions, and the form builds live: a checklist and a preview assemble together, with your logo, colors and font from the Branding Center and a template picked for the job. Try another template from the chat, then open the draft.

**Refine with AI.** From the builder, ask for changes such as `add a phone number field and switch to the Cover template`, or `use the Minimal template and add a payment step`.

**Style.** A Style step offers four templates (Classic, Spotlight, Cover, Minimal) with live thumbnails. The Branding Center drawer edits the shared brand, and synced forms update in the preview as you pick colors and fonts.

**Start from scratch, or open any form.** Start from scratch opens the same builder with inline validation. Every row in the forms list opens in the builder too.

**Future concepts.** Conditional fields, payments and appointment booking are labelled as future concepts. Add a payment or booking step from Add a step, add a condition from a field's menu, or open the Service Request Form, which has all three.

## Phone version

`mobile.html` is the same flow on a phone, for the Mobile section of the case study. On a desktop it shows inside a phone frame; on a phone it fills the screen.

**The owner's side.** From the forms list, open Thryv AI, pick a common form and tap an answer. The form builds with the same checklist and live preview as on desktop, and you can try templates from the chat, then open the builder's Style step, publish, and share from a sheet (copy the link, text, email, QR code).

**The customer's side.** See it as a customer opens the published form in an in app browser, in any of the four templates. Fields are 52 pixels tall with 16 pixel text so iOS doesn't zoom, labels float up as you type, and Submit stays pinned to the bottom.

Deep links: `mobile.html#forms`, `#ai`, `#questions`, `#build`, `#result`, `#builder/<template>`, `#share/<template>`, `#fill/<template>`, `#thanks/<template>`, where the template is `classic`, `spotlight`, `cover` or `minimal`. Add `?rec` to draw a touch where each tap lands, for screen recordings.

## Run it

There is no build step. Serve the folder and open it in a browser:

```bash
npx serve .
```

## Deep links

Each starting point has its own address, for example `index.html#ai/style` or `index.html#future/pay`.

| Start | Points |
| --- | --- |
| `ai` | `list`, `ai-welcome`, `ai-clarify`, `ai-generated`, `details`, `fields`, `style`, `settings`, `share`, `done` |
| `manual` | `list`, `details`, `fields`, `style`, `settings`, `share`, `done` |
| `future` | `cond`, `pay`, `appt` |

## Notes

* AI replies come from scripted rules, not a live model, so the demo behaves the same every time. Prompts about intake, leads, events, feedback or bookings each get their own questions, fields and template.
* Template and brand changes use the View Transitions API where the browser supports it, and fall back to an instant change elsewhere. Motion respects reduced motion settings.
* `video/tour.mp4` is a recorded walkthrough of the AI flow. The intro offers it as Watch the tour.
* All names, forms and the Otter and Rocket brand are demo data.
* `index.html` holds the whole prototype. `img/otter-and-rocket.jpg` is the demo logo used in the form preview.
