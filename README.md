# RHM Headshots

Employee headshots for the RHM newsletter and other marketing work. This repo is just for storing and pulling photos.

## How files are named

Every photo file has the person's name somewhere in the file name. Some also include a location or job title. For example:

- `John Smith.jpg`
- `john-smith-2026.png`
- `Headshot_JohnSmith_edited.jpg`
- `John Smith - Phoenix.jpg`
- `John Smith Account Manager.png`

To find someone, search the file names for their first and last name. Ignore capital letters, spaces, dashes, and underscores when matching. Ignore everything else in the file name too, like location or job title.

## How to pull a photo

Replace `OWNER` with the GitHub username and `REPO` with this repo's name.

**1. List every file in the repo**

```
https://api.github.com/repos/OWNER/REPO/contents/
```

This returns a list of files. Each one has a `name` and a `download_url`.

**2. Find the person**

Look for the file whose `name` contains the person's name.

**3. Download it**

Use that file's `download_url`. It looks like this:

```
https://raw.githubusercontent.com/OWNER/REPO/main/FILE-NAME.jpg
```

If the file name has spaces, replace each space with `%20` in the link.

## Example (command line)

```bash
# list files
curl -s https://api.github.com/repos/OWNER/REPO/contents/ | grep '"name"'

# download one
curl -L -o "John Smith.jpg" "https://raw.githubusercontent.com/OWNER/REPO/main/John%20Smith.jpg"
```

## If more than one file matches

If two people have the same name, use the extra details in the file name (location or job title) to pick the right one. If the extra details still don't make it clear, check with the repo owner before using either.

## Adding photos

1. Make sure the photo is edited and is the newest version.
2. Don't use photos where the person is holding a name tag or sign, or standing in front of a whiteboard.
3. Put the person's name in the file name.
4. Upload it to the main folder of this repo.
