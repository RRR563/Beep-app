# Beep — Build your APK with GitHub (no software needed on your computer)

GitHub will compile the Android app for you in the cloud, for free.
You only need a web browser.

## Step 1 — Create a GitHub account
Go to https://github.com and sign up (free). Verify your email.

## Step 2 — Create a new repository
1. Click the "+" at the top right → "New repository"
2. Repository name: `beep-app` (any name works)
3. Choose **Public** (cloud builds are free and unlimited for public repos)
4. Click "Create repository"

## Step 3 — Upload the app files
1. On the empty repository page, click "uploading an existing file"
2. Drag and drop these from the unzipped folder:
   - the `www` folder
   - `capacitor.config.json`
   - `package.json`
3. Click "Commit changes"

## Step 4 — Add the build robot (workflow file)
The `.github` folder is hidden on most computers and often won't drag,
so create it by hand — it takes 30 seconds:
1. In your repository, click "Add file" → "Create new file"
2. In the filename box, type exactly:
   `.github/workflows/build-apk.yml`
   (typing each `/` creates a folder automatically)
3. Open the file `build-apk.yml` from this zip in Notepad,
   copy ALL of it, and paste it into the big text box on GitHub
4. Click "Commit changes"

## Step 5 — Wait for the build, then download
1. Click the "Actions" tab at the top of your repository
2. You'll see "Build Beep APK" running (yellow dot). Wait ~5 minutes
   until it turns into a green checkmark.
3. Go to your repository's main page → click "Releases" (right side)
   → download **Beep.apk**

Tip: open the Releases page on your phone's browser and download the
APK directly there — then just tap it to install. Android will ask to
allow installing unknown apps; allow it (normal for non-Play-Store apps).

## Updating the app later
Whenever you edit and re-upload `www/index.html`, GitHub automatically
rebuilds the APK. The Releases page always has the newest version.
