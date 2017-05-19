# Migrating your package

## First Steps

We aim to make migrating your package an easy and straight-forward process. 
To get started, open an issue in this repository. There's no set template for
it, but you could title it something like `Request for Migration`. The body
could look something like this:

```md
Hello, I would like to migrate [REPOSITORY] to Fruitful.
```

That's all - you don't need to explain yourself for wanting to hand over
maintenance. We understand, that's why we're here. Of course, you can add a
description of what your project is about or anything you'd like, really.

## Transferring

After you've made your request, one of our owners is going to invite you into
our GitHub organization. At this point, you should be able to transfer your
repository using GitHub's included tools.

Of course, your repository is going to enjoy the same benefits that all others
have, such as access to our tooling (Danger, Greenkeeper, Travis, etc.) and our
community.

## npm module transferring

It's not required, but if you want to, you can move your npm package under the
`@fruitful` scope. This process is rather simple, just tell us that you would
like to move your package under our scope in your issue and we will invite you
to our npm organization. Once that's done, you can rename the `name` field in
your `package.json` to this:

```json
"name": "@fruitful/<your-package-name>"
```

Then, you can simply run `npm publish` to republish your package under our
scope. Of course, you should also update your documentation to reflect this
change.

It is also advisable that you deprecate the old name of your package. You can
do this by running the following command:

```sh
npm deprecate <your-old-package-name> "This package is now available at @fruitful/<your-package-name>"
```

_(This document is a living document. The process of migration might change as
time goes on, and as such, this document will get updated as well)_

