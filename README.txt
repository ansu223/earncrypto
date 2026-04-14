=============================================
  HYTALE - LANDING PAGE SETUP GUIDE
=============================================

WHAT IS THIS?
-------------
A content locker landing page designed for the Hytale game niche.
Users are guided through a multi-step flow (edition selection, account
connection, progress animation) before reaching a verification step
that loads your OGAds content locker.


HOW TO SET YOUR OGADS LOCKER LINK
----------------------------------
1. Open the file: js/main.js
2. Find line 4 at the very top:

     const OGADS_LOCKER_URL = "YOUR_OGADS_LOCKER_LINK_HERE";

3. Replace YOUR_OGADS_LOCKER_LINK_HERE with your actual OGAds locker URL.
   Example:

     const OGADS_LOCKER_URL = "https://locker.ogads.com/your-link-here";

4. Save the file. That's it!


HOW TO CUSTOMIZE COLORS & FONTS
---------------------------------
1. Open the file: css/style.css
2. At the very top you'll see the :root section (around line 8):

     --gold: #d29f32;          <-- Main gold accent color
     --gold-light: #ecbc62;    <-- Lighter gold variant
     --bg: #15243a;            <-- Page background (deep navy)
     --text: #dce8eb;          <-- Main text color
     --font-heading: 'Lexend', sans-serif;
     --font-body: 'Nunito Sans', sans-serif;

3. Change any of these values to customize the look.
4. To change fonts, update the Google Fonts link in index.html (line 11)
   AND the --font-heading / --font-body values in style.css.


HOW TO CUSTOMIZE TEXT & CONTENT
--------------------------------
All page text is in index.html. Open it and search for the text you
want to change. Key sections:

  - Hero headline:    Search for "Get Your Free Hytale Key"
  - Hero subtitle:    Search for "Unlock the full adventure"
  - Edition details:  Search for "plan-card" to find each edition
  - Progress messages: Open js/main.js and search for "phases" to
    edit the progress bar status messages


HOW TO UPLOAD / DEPLOY
-----------------------
Option A - Netlify (easiest, free):
  1. Go to https://app.netlify.com
  2. Drag and drop the entire "Hytale" folder onto the page
  3. Done! You'll get a live URL instantly

Option B - cPanel / traditional hosting:
  1. Log into your hosting control panel
  2. Open File Manager -> navigate to public_html (or your domain folder)
  3. Upload all files keeping the folder structure:
       index.html
       css/style.css
       js/main.js
       img/ (if you have images)
  4. Visit your domain to confirm it works

Option C - GitHub Pages (free):
  1. Create a new GitHub repository
  2. Upload all files to the repository
  3. Go to Settings -> Pages -> set source to "main" branch
  4. Your page will be live at https://yourusername.github.io/repo-name


HOW TO TEST BEFORE GOING LIVE
-------------------------------
1. Open index.html directly in your browser (double-click the file)
2. Click "Get Started" and go through each step
3. Check that:
   - All animations are smooth (floating particles, progress bar)
   - Mobile layout works (resize your browser to a narrow width)
   - The verification step shows an alert saying "Locker URL not
     configured" (this is correct if you haven't set your link yet)
4. After setting your OGAds link, test again to make sure the locker
   loads in the popup overlay
5. Try on a real phone if possible to verify the mobile experience


FILE STRUCTURE
--------------
Hytale/
  index.html       - The main landing page
  css/style.css    - All styles (colors, layout, animations)
  js/main.js       - All logic (flow, particles, progress bar, locker)
  img/             - Place any images here (logo, backgrounds)
  README.txt       - This file
