# Feel Events website: going live

This folder is the whole website. It goes live through three free accounts:

- **GitHub** stores the website's files.
- **Netlify** puts the website on the internet.
- **The admin page** at `yourdomain/admin` is where you post events. It saves straight to GitHub, and Netlify updates the live site within about a minute.

It takes about 30–45 minutes, once.

---

## 1. Put the files on GitHub

1. Create a free account at https://github.com.
2. Click **+ → New repository**.
   - Name: `feel-events`
   - Visibility: **Public**. The site is public anyway, and this keeps it on the free plan.
   - Click **Create repository**.
3. On the new repository page, click **uploading an existing file**.
4. Drag in **everything inside** this `feel-events` folder: `index.html`, `netlify.toml`, `SETUP.md`, and the `admin`, `data` and `images` folders. Then click **Commit changes**.
5. Open `admin/config.yml` on GitHub and click the pencil icon. Change
   `repo: YOUR-GITHUB-USERNAME/feel-events` to your real username, for example `repo: feelevents/feel-events`. Click **Commit changes**.

## 2. Put the site online with Netlify

1. Create a free account at https://www.netlify.com and sign up with your GitHub account.
2. Click **Add new site → Import an existing project → GitHub**, then choose `feel-events`.
3. Leave the build settings empty and click **Deploy**.
4. After a minute your site is live at an address like `something.netlify.app`. Open it to check.

## 3. Turn on the admin login

The admin page logs you in with GitHub. GitHub has to be told about your site once:

1. On GitHub: **Settings → Developer settings → OAuth Apps → New OAuth App**.
   - Application name: `Feel Events admin`
   - Homepage URL: your Netlify address, for example `https://something.netlify.app`
   - Authorization callback URL: `https://api.netlify.com/auth/done`
   - Click **Register application**, then **Generate a new client secret**. Keep this page open.
2. On Netlify, open your site and find **OAuth** under the site's access-control settings. The exact menu name moves now and then; search the site settings for "OAuth".
   - Click **Install provider → GitHub**.
   - Paste the **Client ID** and **Client secret** from GitHub and save.
3. Go to `https://something.netlify.app/admin` and click **Login with GitHub**.

## 4. Your own domain (optional)

1. Buy the domain, for example `feelevents.co.za`, from any .co.za registrar, or directly in Netlify under **Domains**.
2. In Netlify: **Domain management → Add a domain**, then follow its steps. Netlify adds the free HTTPS certificate itself.
3. On GitHub, open the OAuth App from step 3 and change the Homepage URL to the new domain.

---

## Posting updates (every week)

Go to **yourdomain/admin** on your phone or computer and log in with GitHub.

| To do this | Open | Then |
|---|---|---|
| Add a special event | **Special events** | **Add event**: name, date, time, entry, flyer → **Publish** |
| Post an announcement | **Announcements** | **Add announcement** → **Publish** |
| Change this week's Thursday or Sunday flyer, or the time | **Weekly nights** | Open the night, replace the flyer → **Publish** |
| Remove something | Open the list | Click the item's **×** → **Publish** |

- Events disappear from the website the day after their date, so you don't need to delete them. Delete old ones now and then to keep the list short.
- Changes show on the live site about a minute after you press Publish.
- Flyers: upload JPG or PNG. Keep them under about 1 MB so the site loads fast on mobile data. Exporting from Canva as **JPG** usually does this.

## Changing fixed details

The table-booking number (073 390 4343), the venue name and the top banner text are written into `index.html`. To change them, ask for an updated file or edit `index.html` on GitHub.
