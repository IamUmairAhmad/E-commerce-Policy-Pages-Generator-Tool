# E-commerce Policy Pages Generator Tool

A single-file HTML tool with three sections. Open `store-policy-generator.html` in any browser. No install and no server are needed; only fetching a product link needs internet.

- **Policy Pages:** writes the store pages Google Merchant Center expects, in a natural, human-sounding tone, from a short form.
- **Humanizer:** paste your own text and get a more natural, human-sounding rewrite. See [Humanizer](#humanizer).
- **Product Details:** fetch a product page (or paste a title and description) and get a rewritten, brand-free product title and description. See [Product Details](#product-details).

## Pages it generates

1. About Us
2. Contact Us
3. FAQs
4. Shipping Policy
5. Privacy Policy
6. Refund & Returns Policy
7. Terms & Conditions
8. Payment Policy
9. Legal Notice

Every page ends with the same "Contact us" block: business name, email, phone, hours with time zone, and address.

### Legal Notice

The Legal Notice is written for the business's selected country and its region. It names the law that applies (for example § 5 DDG in Germany, LCEN article 6-III in France, the Companies Act 2006 in the UK, the Australian Consumer Law, Japan's Act on Specified Commercial Transactions) and uses that country's own labels, such as "VAT ID (USt-IdNr.)", "SIREN / SIRET" or "ABN". Germany, Austria and Switzerland get an Impressum-style notice, and France gets the publication director and website host lines. Other countries get a plain legal notice with a regional paragraph.

Fill in the **Legal details** section of the form (legal company name and form, registration number, VAT or tax ID, authorised representative, website host and so on). A hint under the heading lists what the chosen country normally needs. Empty fields are left out of the page instead of showing placeholders. The notice is a template based on the main rules for each country, so have it checked against the laws that apply to your business.

## Humanizer

Switch to the **Humanizer** tab, paste any text you wrote (a product description, an About Us section, a policy paragraph, an email) and click **Humanize**. It works as plain text, or as HTML, in which case your tags, links and headings are left untouched and only the readable text changes.

What it does:

- Swaps stiff or stock wording for plain words ("utilize" becomes "use", "prior to" becomes "before", "in order to" becomes "to")
- Cuts filler and stock phrases ("It is important to note that", "In today's fast-paced world")
- Replaces stiff connectors ("Furthermore," "Moreover," "In conclusion,") with everyday ones
- Adds contractions, breaks up very long sentences, and tidies em dashes and semicolons
- Varies the rhythm: joins two very short sentences, rewords a third repeated opener ("We... We... We..."), breaks up a run of equally long sentences, and turns stiff passive lines into active ones ("Orders are processed within 2 days" becomes "We process orders within 2 days") when you already write as "we"
- Replaces brochure wording such as "committed to providing", "plays a key role in", "unlock the potential", "customer satisfaction is our top priority"
- Leaves emails, links, times, prices and abbreviations exactly as written

Controls and tools:

- **Mode:** Standard, Fluency (light touch), Formal (writes out contractions, fuller wording), Simple (plainer words, shorter sentences), Shorten (cuts padding) or Creative (rewrites harder). **Compare modes** shows the same text in all six side by side, with a "Use this version" button on each
- **Strength:** Light, Balanced or Strong. **Tone:** Professional, Friendly or Casual (Casual adds an occasional spoken-style opener and is skipped automatically on legal or policy wording)
- **Word variety:** a slider that swaps more words for close alternatives from a built-in thesaurus
- **Words to keep as they are:** list brand and product names (comma-separated) and they are never touched
- **English spelling:** keep as written, or convert to American or British spelling
- **What to change:** turn any of the six kinds of edit on or off
- **Review changes:** highlights every word that changed, and lets you click a word to pick another from the thesaurus
- **Paste and Upload file:** paste from the clipboard, or load a .txt, .md or .html file (for Word files, copy the text and paste it)
- **History:** your last 15 rewrites are kept in this browser, with a Restore button
- **Another version:** same text, different wording. **Humanize** always gives the same result for the same text and settings
- **Output:** before/after word count, average sentence length, reading ease, a human-style score, a tone read-out and a count of stock "template" phrases, plus a "What changed" list, an HTML preview, and Copy, Copy as plain text, Download and Use as input buttons

The human-style score is this tool's own reading check (template phrases, sentence-length variety, contractions, repeated openers). It is not an AI-detector result.

It uses built-in writing rules that run in your browser. Nothing is uploaded, and no AI service is involved. It makes text read more naturally, but it cannot promise any particular result in an AI-detection tool, so read the result once and add your own details. There is no "expand" or free-form "custom instruction" mode, because those need a language model.

## Product Details

Two ways to start:

1. **From a product link.** Paste a product page URL and click **Fetch**. The title, description and bullet points are read from the page (structured product data first, then page tags).
2. **From my own text.** Type or paste a title and description.

Then **Rewrite product details**. The text goes through the Humanizer rules, brand names are removed from the title and description (known brands, the fetched page's own brand and store name, and any names you add), and the title is cleaned (shouting caps, "Free Shipping" style filler and repeated words removed, optional length limit). Copy the title, the description, HTML, or both.

Limits to know about:

- Browsers block reading other websites directly. If a direct fetch fails, the tool can retry through public CORS proxies (a tick box, on by default). The page address then passes through that third-party service. Untick it, or enter your own proxy URL with `{url}` in it, if that matters. Sites that block automated requests (Amazon, AliExpress and Alibaba often do) will fail: open the page, select all, copy, and paste it into "Paste the page text or source instead" (the first line becomes the title), or use "From my own text".
- Product names such as "iPhone" become generic words ("smartphone"). Names that are also ordinary words (Apple, Gap) are only removed with a ®/™ mark, "by X", a possessive, or when you list them yourself. Check the "Extra brand names" box.
- Check the result against the real product. A rewrite of another store's text is still based on it, so add your own details.

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
- **Contact form:** the Contact Us page can mention a contact form, but the form itself is not generated. A pasted HTML form cannot send mail on either platform, so add it with Shopify's contact page template or a WordPress form plugin.
- **Legal Notice:** details that are not required where you sell can be left empty. The EU online dispute resolution platform closed in July 2025, so the notice does not link to it.
- **Countries:** pick "Other country" if yours is not on Google's list (for example Pakistan), type it in, and choose the currency.
- **No returns:** choosing "No, I don't accept returns" hides both Refund Method and Refund Processing Time.
- **Cash on Delivery:** if it is selected as a payment method, the refund wording explains that those orders are refunded by bank transfer and that the bank-details email comes only from your business email.
- **Not legal advice:** the output is a template. Have the Privacy Policy and Terms reviewed for the laws that apply in your target country.
- **Country list:** based on Google's [supported languages and currencies](https://support.google.com/merchants/answer/160637) table.

## License

See [LICENSE](LICENSE).
