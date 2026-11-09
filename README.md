# Form builder with AI

Interactive prototype of a unified form builder with AI generation. Describe a form to Thryv AI, answer two quick questions, then review, refine and publish it in the same builder used for forms built by hand.

Built from the Figma design on demo data, as a companion to the Form Unification case study at [dbyxdesign.com](https://dbyxdesign.com/case-form-unification.html).

## Two flows

**AI flow.** Forms list, Create with AI, Thryv AI opens in a new tab, clarifying questions, the generated draft hands back to the builder tab, then fields, settings, publish and share.

**Manual flow.** Forms list, Start from scratch, details with inline validation, fields, settings, publish and share.

**Future concepts.** Three features designed as future states, shown as steps of one form: conditional fields (an If and Then rule that shows a question only for certain answers), payments (products, upsells and promo codes with a live cart total) and appointment booking (a calendar with open times).

Back and Next (or the arrow keys) step through each scene. Everything in between is clickable: type your own prompt, ask for changes such as `add a phone number field and make company name optional`, drag fields to reorder, change styles and watch the preview update.

## Run it

There is no build step. Serve the folder and open it in a browser:

```bash
npx serve .
```

## Deep links

Each scene has its own address, for example `index.html#ai/fields` or `index.html#manual/settings`.

| Flow | Scenes |
| --- | --- |
| `ai` | `list`, `ai-welcome`, `ai-clarify`, `ai-generated`, `details`, `fields`, `settings`, `share`, `done` |
| `manual` | `list`, `details`, `fields`, `settings`, `share`, `done` |
| `future` | `cond`, `pay`, `appt` |

## Notes

* AI replies come from scripted rules, not a live model, so the demo behaves the same every time. Prompts about intake, leads, events, feedback or bookings each get their own questions and fields.
* All names, forms and the Otter and Rocket brand are demo data.
* `index.html` holds the whole prototype. `img/otter-and-rocket.jpg` is the demo logo used in the form preview.
