# E-commerce Policy Pages Generator Tool

A single-file HTML tool with two sections. Open `store-policy-generator.html` in any browser. No install, no server and no internet connection are needed.

- **Policy Pages:** writes the store pages Google Merchant Center expects, in a natural, human-sounding tone, from a short form.
- **Humanizer:** paste your own text and get a more natural, human-sounding rewrite. See [Humanizer](#humanizer).

## Pages it generates

1. About Us
2. Contact Us
3. FAQs
4. Shipping Policy
5. Privacy Policy
6. Refund & Returns Policy
7. Terms & Conditions
8. Payment Policy

Every page ends with the same "Contact us" block: business name, email, phone, hours with time zone, and address.

## Humanizer

Switch to the **Humanizer** tab, paste any text you wrote (a product description, an About Us section, a policy paragraph, an email) and click **Humanize**. It works as plain text, or as HTML, in which case your tags, links and headings are left untouched and only the readable text changes.

What it does:

- Swaps stiff or stock wording for plain words ("utilize" becomes "use", "prior to" becomes "before", "in order to" becomes "to")
- Cuts filler and stock phrases ("It is important to note that", "In today's fast-paced world")
- Replaces stiff connectors ("Furthermore," "Moreover," "In conclusion,") with everyday ones
- Adds contractions, breaks up very long sentences, and tidies em dashes and semicolons
- Leaves emails, links, times, prices and abbreviations exactly as written

Controls:

- **Strength:** Light, Balanced or Strong
- **Tone:** Professional, Friendly or Casual (Casual adds an occasional spoken-style opener, so keep it off legal pages)
- **What to change:** turn any of the five kinds of edit on or off
- **Another version:** same text, different wording. **Humanize** always gives the same result for the same text and settings
- **Output:** before/after word count, average sentence length and reading ease, a "What changed" list, an HTML preview, and Copy, Copy as plain text, Download and Use as input buttons

It uses built-in writing rules that run in your browser. Nothing is uploaded, and no AI service is involved. It makes text read more naturally, but it cannot promise any particular result in an AI-detection tool, so read the result once and add your own details.

## How to use the Policy Pages section

1. Open `store-policy-generator.html` in your browser.
2. Fill in the form. Business Name is required, and the more fields you complete, the more specific the pages become.
3. Click **Generate pages**, then switch between the tabs to review each page.
4. Click **Copy HTML** (or **Copy plain text**) for the current page, or **Download all pages (.html)** for everything in one file.
5. Click **Rewrite wording** to get a differently worded version of the same content.

Your form entries are saved in your browser's local storage, so they are still there next time. Nothing is sent anywhere.

## Pasting into Shopify or WordPress

Copied HTML uses only `h2`, `p`, `ul`, `strong`, `a` and `br`, which both platforms accept. The page title (H1) is left out by default because both platforms already use the page title as the H1. A checkbox adds it back.

- **Shopify:** Pages → open the page → click the `<>` "Show HTML" button in the editor and paste.
- **WordPress:** add a "Custom HTML" block (or use the Classic editor's Text tab) and paste.

## What you can configure

**Business details**
- Business name, website, email, phone and address
- Business hours (preset options or custom) and time zone (worldwide list in `(GMT-05:00) Eastern Standard Time (New York)` format)
- Founded year, store products, brand message, owner details and team introduction

**Location and currency**
- Shipping & refund country, chosen from the countries supported by Google Merchant Center
- Currency is selected automatically from the country, and you can change it to any other currency
- The country is also used as the governing law and dispute resolution location

**Orders and shipping**
- Order cut-off time (AM/PM, followed by your time zone), order cancellation time
- Handling time and transit time. Business-hours day names (for example "Monday - Friday") are added automatically
- Total delivery time, calculated automatically from handling plus transit
- Shipping costs, shipping methods, carriers and shipping restrictions

**Returns and refunds**
- Whether you accept returns for all products, for defective products only, or not at all
- Exchanges, return window (including Lifetime), and product condition for returns
- Return methods (in store, drop-off location, by mail) and return label option
- Restocking fee (none, fixed amount or percentage)
- Refund method, refund processing time and refund currency. If the method is bank transfer, the pages say refund emails come only from your business email address

**Payments**
- Accepted payment methods, plus any custom ones

Email addresses in the generated pages are clickable `mailto:` links. Order-change and privacy contacts use your business email and phone.

## Google Merchant Center coverage

The pages are written to include what Merchant Center reviewers look for, such as:

- **Privacy Policy:** data collected, how it is used, third-party sharing, customer rights and contact details
- **Terms & Conditions:** introduction, user obligations, orders and payment, liability, dispute resolution and amendments
- **Shipping Policy:** methods and carriers, costs, delivery times, regions served and restrictions
- **Refund & Returns Policy:** eligibility, return process, fees, refund timing and exchanges
- **About Us:** background, mission and values, brand message, address, owner and team
- **Contact Us:** address, email, phone and optional contact form

## Notes

- **Unique wording:** each generation uses a fresh random seed, shuffles list order where order does not matter, and swaps common phrases, so two runs never read the same. Policy pages share a standard structure, so some similarity between stores is normal. Add a personal sentence or two, especially in About Us and the owner bio.
- **Contact form:** the Contact Us page can mention a contact form, but the form itself is not generated. Add it with Shopify's contact page template or a WordPress form plugin.
- **Not legal advice:** the output is a template. Have the Privacy Policy and Terms reviewed for the laws that apply in your target country.
- **Country list:** based on Google's [supported languages and currencies](https://support.google.com/merchants/answer/160637) table.

## License

See [LICENSE](LICENSE).
