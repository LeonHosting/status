# cState Site v6

This is the default cState status page website directory/folder.

* Example site repository link (you are here): https://github.com/cstate/example
* Main cState source code repository: https://github.com/cstate/cstate

## Deployment

Recommended for this repository: Cloudflare Pages with GitHub integration.

Cloudflare Pages settings:

* Framework preset: None
* Build command: `hugo --gc --minify`
* Build output directory: `public`
* Environment variable: `HUGO_VERSION=0.163.0`

For production on `https://status.leonhosting.de`, keep `baseURL` in
`config.yml` set to that domain and add the custom domain in Cloudflare Pages.
If you prefer preview deployments to use their `pages.dev` preview URL as the
canonical URL, use `hugo --gc --minify -b $CF_PAGES_URL` instead.

When cloning locally, include the cState theme submodule:

```sh
git clone --recursive https://github.com/LeonHosting/status.git
```

For an existing checkout:

```sh
git submodule update --init --recursive
```

## Are you updating? Use these commands

Download your site with all the directories. `git clone --recursive <your repo link goes here>`

Update the cState theme submodule. `git submodule foreach git pull origin master`

In the parent directory, type `hugo serve`. Check to see if everything is working.

Then do `git add -A; git commit -m "Update cState"; git push origin <branch, probably main or master>`. Your status page is now updated and uploaded.


## For maintainers (probably not for you)

Maintainers need to update both cstate/cstate and cstate/example for each new version.

Download this repo with all the directories. `git clone --recursive -b master https://github.com/cstate/example.git`

Add your changes from cstate/cstate's exampleSite folder.

Update the cState theme submodule. `git submodule foreach git pull origin master`

Then push `git add -A; git commit -m "Update cState vX.X.X"; git push origin master`.

## License

MIT © Mantas Vilčinskas
