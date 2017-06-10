# Maintenance

### What happens when a project is first transferred to fruitful?
When a project is first transferred to fruitful it will:

- Adopt our code of conduct and enforcement policy
- Move to the `fruitful` GitHub organisation
- Update to use fruitful's standards for testing, linting, documentation, etc.
- Get listed on the fruitful project website.
- Once in shape, a new release should be made in its old namespace, that deprecates it, and points to the new namespace.

You can read more about the transfer process on the [migrating](MIGRATING.md) page.

### What does day-to-day maintenance in the fruitful community look like?

- Managing the issue tracker
- Keeping dependencies up to date (with the help of https://greenkeeper.io/)
- Fixing reported bugs & security issues
- Responding to feature requests
- Improving and updating documentation and automated tests

#### Managing the issue tracker

This essentially means having more people actively maintain your project.
After you migrate your project, it will be assigned a [category](http://github.com/fruitfuljs/docs/blob/master/CONTRIBUTING.md#Categories), and all contributors belonging to that category will receive __write__ access to your repository.
No worries though, you can (and are encouraged to) protect your main branch, in order to enable contributing only by pull request.

#### Keeping dependencies up to date

A project under fruitful can choose to use [Greenkeeper](http://greenkeeper.io) to automatically monitor and upgrade its dependencies.
This requires a project to have a test suite, because otherwise Greenkeeper can't ensure that the new dependency version doesn't break anything in the project's code.

#### Fixing reported bugs & security issues

Much of this includes what is described in `Managing the issue tracker`, but there are separate tools used when releasing new versions of your project.
fruitful uses [semantic-release](https://github.com/semantic-release/semantic-release), which makes releasing new GitHub/npm versions painless and automated.
It also generates a changelog.

Using semantic-release and Greenkeeper works better when using the [AngularJS commit message conventions](https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit).
It makes formatting commit messages easier and also enables verbose changelogs to be automatically generated.
This is not enforced (neither is the usage of semantic-release), but from experience, projects more than greatly benefit from using it.

#### Responding to feature requests

See `Managing the issue tracker`.

#### Improving and updating documentation and automated tests

See `Managing the issue tracker`.

### Stopping maintenance
If a project is unused or we're no longer able to support it, we may decide to stop maintaining it.
If this happens, we'll clearly mark the project as unmaintained or deprecated in its README.

If someone outside the fruitful project wants to continue maintaining the project and forks it, we can update the README to point to the maintained fork.
