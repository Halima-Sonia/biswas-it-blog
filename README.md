# Biswas IT Firm — Blog Website

এটি একটি responsive, দুই পৃষ্ঠার Blog Website। এটি তৈরি করা হয়েছে শুধু **HTML5 ও CSS3** দিয়ে। এখানে কোনো JavaScript বা framework ব্যবহার করা হয়নি।

## প্রজেক্টে যা আছে

- `index.html` — Blog List Page; CSS Grid-এ সাজানো ৬টি Blog Card।
- `article.html` — সম্পূর্ণ Blog Article Page; readable typography, quote, list এবং table-সহ।
- `styles.css` — দুই পৃষ্ঠার shared styling, CSS variables, hover transition এবং responsive breakpoints।
- `README.md` — প্রজেক্টের বিবরণ ও চালানোর নির্দেশনা।

## নিজের কম্পিউটারে চালানোর নিয়ম

১. ZIP ফাইলটি Download করে Extract করেন।
২. Extract করা `biswas_it_blog` ফোল্ডারটি খোলেন।
৩. `index.html` ফাইলটি Browser-এ খোলেন।
৪. যেকোনো Blog Card-এ ক্লিক করলে `article.html` পৃষ্ঠায় যাবে। Article Page-এর “Back to all articles” লিংকে ক্লিক করলে Blog List-এ ফিরে আসবে।

চাইলে VS Code-এর **Live Server** extension দিয়েও প্রজেক্টটি চালাতে পারেন।

## CSS Variable কী?

CSS Variable বা Custom Property হলো এমন একটি reusable value, যেটি CSS-এর একাধিক জায়গায় ব্যবহার করা যায়। এই প্রজেক্টে Variable-গুলো `styles.css` ফাইলের `:root`-এর মধ্যে রাখা হয়েছে।

উদাহরণ:

```css
:root {
  --color-brand: #ff725e;
  --color-ink: #172b3a;
  --font-body: "DM Sans", sans-serif;
  --text-base: 1rem;
  --text-display: clamp(2.8rem, 7vw, 5.8rem);
}

Variable ব্যবহার করতে `var()` লিখতে হয়:

```css
body {
  color: var(--color-ink);
  font-family: var(--font-body);
  font-size: var(--text-base);
}


### এই Variable-গুলো কী কাজ করে?

- `color-brand`: ওয়েবসাইটের প্রধান Coral রং।
- `color-ink`: Heading ও Text-এর মূল রং।
- `font-body`: সাধারণ লেখার Font।
- `text-base`: সাধারণ লেখার Font Size।
- `text-display`: বড় Heading-এর responsive Font Size। `clamp()`-এর কারণে স্ক্রিনের আকার অনুযায়ী Font Size বদলায়, তবে নির্ধারিত সীমার বাইরে যায় না।

**সুবিধা:** কোনো রং বা Font Size পরিবর্তন করতে হলে সংশ্লিষ্ট Variable একবার পরিবর্তন করলেই হয়। এতে Design consistent থাকে এবং CSS maintain করা সহজ হয়।

## CSS Grid ও Hover Animation

Blog List Page-এ ছয়টি Card সাজানোর জন্য CSS Grid ব্যবহার করা হয়েছে। বড় স্ক্রিনে তিনটি, মাঝারি স্ক্রিনে দুটি এবং ছোট মোবাইল স্ক্রিনে একটি Card প্রতি Row-তে দেখা যাবে।

Card-এর Hover Animation CSS `transition` দিয়ে করা হয়েছে। Mouse Card-এর ওপর নিলে Card সামান্য ওপরে ওঠে, Shadow দেখা যায় এবং Image একটু Zoom হয়। এর জন্য JavaScript দরকার হয় না।

## প্রজেক্টে অন্তর্ভুক্ত বিষয়

- ৬টি Blog Card
- CSS Grid Layout
- Category Tag
- Card Hover Animation (`transition`)
- Blog Article Page
- পাঠযোগ্য Line Height ও Content Width
- Heading, Quote, List ও Table Style
- CSS Variable
- দুই HTML Page-এর মধ্যে Navigation Link
- Desktop, Tablet ও Mobile-এর জন্য Responsive Design