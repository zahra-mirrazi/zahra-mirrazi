# Moving zahra-mirrazi.com from Wix to GitHub Pages

This folder is your whole website. Hosting it on GitHub Pages is free. The only cost is the domain name itself, about €10–15 a year.

Do the steps in this order, and don't cancel Wix until the new site is live.

## Step 1. Save your files from Wix (do this first)

Your new CV is already included as `files/cv.pdf`. Your photo and several PDFs are still stored on Wix and will disappear when you cancel. Open each link below while Wix is still active, save the file, and rename it to the name on the left. Put the PDFs in the `files` folder and the photo in the `images` folder.

| Save as | Download from |
|---|---|
| images/profile.jpg | Your profile photo (right-click it on your Wix home page and choose "Save image as…") |
| files/sicogg23-neg-raising.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_a73bf2a8c4f34e3d8c6e0231d473125d.pdf |
| files/generals-paper-aspect-splits.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_2200c8a6d5ed4eb2a13aa43d833ceb02.pdf |
| files/igg50-mood.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_c0bed12dd8384cd49006bb23c75bf087.pdf |
| files/wossp19-indefinites.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_5f002e8a08e24c578901f38017be3cd9.pdf |
| files/wossp19-embedded-tenses.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_28930c71a73443dab80705726323e9d5.pdf |
| files/sub28-poster.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_9fa58e726984418a9bf3935d958115d3.pdf |
| files/triplea10-perfectivity.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_a654896203a24552ba3335aa14f5aa38.pdf |
| files/wccfl41-choice-functions.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_c258dfe7b503402baff7659c1fcc02bf.pdf |
| files/wccfl41-modal-past.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_4587df67c42541a9be680657d800e9fb.pdf |
| files/cls58-missing-words.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_6a89eb02e6b346c28d4f4573bfa1d54d.pdf |
| files/lsa2022-neg-raising.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_224cead4b793418ba2d1754ef7d6675b.pdf |
| files/lsa2022-functional-indefinites.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_c043dc3e1e72404a8bafb169fd5f4cda.pdf |
| files/hse2021-functional-indefinites.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_e503b46e2d6a44f5b77026df290f7905.pdf |
| files/esslli2021-skolemization.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_21120ebc967842389b5e115d35af78f6.pdf |
| files/iatl36-neg-raising.pdf | https://www.zahra-mirrazi.com/_files/ugd/26df49_66cacfb58ee14a62938ac5cec3207465.pdf |

The Talks page now follows your new CV. Only the talks that had slides on Wix have a slides link. If you have slides for others, add them the same way.

**Update two links in your CV.** Your CV links to two PDFs stored on Wix. After the move, change them to:

- SICOGG 23 paper: https://www.zahra-mirrazi.com/files/sicogg23-neg-raising.pdf
- Generals paper: https://www.zahra-mirrazi.com/files/generals-paper-aspect-splits.pdf

Then replace `files/cv.pdf` on GitHub with the updated CV.

## Step 2. Put the site on GitHub

1. Create a free account at github.com. Your username becomes part of the free address, for example `zmirrazi.github.io`.
2. Click **New repository**. Name it exactly `yourusername.github.io` (with your real username), set it to **Public**, and click **Create repository**.
3. On the new repository page, click **uploading an existing file**. Drag in everything from this folder: the `.html` files, `style.css`, `CNAME`, `.nojekyll`, and the `files` and `images` folders. Click **Commit changes**.
   - `.nojekyll` and `CNAME` may be hidden on a Mac. Press Cmd + Shift + . in Finder to show them.
4. Go to **Settings → Pages**. Under "Build and deployment", choose **Deploy from a branch**, branch **main**, folder **/ (root)**, and save.
5. After a minute or two, the site is live at `https://yourusername.github.io`. Check it before going further.

## Step 3. Move your domain away from Wix

1. In Wix, go to **Domains**, click the **⋯** next to zahra-mirrazi.com, and choose **Transfer away from Wix → Transfer Domain → I Still Want to Transfer**.
2. Wix emails an authorization code (EPP code) to the domain's registrant email. Check you can still receive mail there.
3. At a new registrar, choose "Transfer a domain", enter zahra-mirrazi.com and paste the code. Inexpensive options include Cloudflare Registrar, Porkbun and INWX (German). The transfer usually takes up to a week, and typically includes one year of renewal.

Note: a domain can't be transferred within 60 days of being registered, transferred, or having its contact details changed.

## Step 4. Point the domain at GitHub

1. In GitHub, go to **Settings → Pages → Custom domain**, enter `zahra-mirrazi.com` and save.
2. At your new registrar, open the DNS settings for zahra-mirrazi.com and add:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | yourusername.github.io |

3. Remove any old A or CNAME records that point to Wix.
4. Wait a few hours. Then, in **Settings → Pages**, tick **Enforce HTTPS**.

## Step 5. Cancel Wix

Only once zahra-mirrazi.com shows the new site and all your PDFs open.

## Updating the site later

Open the page on GitHub (for example `research.html`), click the pencil icon, edit the text, and click **Commit changes**. The live site updates within a minute or two. To add a paper, copy an existing `<li> … </li>` block and change the title, details and link.
