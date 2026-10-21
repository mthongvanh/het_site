# het_site

The public page for Het's projects, served at
[het.tveye.io](https://het.tveye.io): Het, Het Voice Studio and
het_framework, what each does, the tools Het's models can call, the models
each runs and where they run.

One static page, `index.html`, with the app icons in `img/`. Nothing is
built: open the file in a browser to see it.

## Keeping it true

The page describes what has shipped. When a project changes in a way
someone would notice (a feature, a tool, a model, a platform, a release),
bring the page up to date. The facts come from each repo's CHANGELOG.md,
Het's `lib/src/tools/` and the model catalogs. Say only what has been
tested: the apps are tested on iOS 26 and macOS 26.

## Downloads

Het Voice Studio's disk image is attached to this repo's releases, which are
public so the page can link to the file directly:
`https://github.com/mthongvanh/het_site/releases/download/voice-studio-v0.1.0/Het-Voice-Studio-0.1.0.dmg`.
The repo holds only the page, so nothing else is exposed by that. For a new
version, build and notarise it in het_voice_studio, attach the disk image
to a new release here (`voice-studio-vX.Y.Z`), put its SHA-256 in the
notes, and change the link and the version on the page.

## Serving it

Vercel serves `main` as it is, with no build (`vercel.json`). The domain,
het.tveye.io, is a CNAME at Gandi to the target Vercel gives.
