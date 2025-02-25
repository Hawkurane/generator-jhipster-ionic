# Contributing to Ionic for JHipster

Are you ready to contribute to Ionic for JHipster? We'd love to have you on board, and we will help you as much as we can. Here are the guidelines we'd like you to follow so that we can be of more help:

- [Questions and help](#question)
- [Issues and Bugs](#issue)
- [Feature Requests](#feature)
- [Submission Guidelines](#submit)
- [Generator development setup](#setup)
- [Coding Rules](#rules)
- [Git Commit Guidelines](#commit)

## <a name="question"></a> Questions and help

This is the Ionic for JHipster bug tracker, and it is used for [Issues and Bugs](#issue) and for [Feature Requests](#feature).

If you have a question on using Ionic for JHipster, or if you need help with your JHipster project, please [read JHipster's help page](http://www.jhipster.tech/help/) and use the [JHipster](http://stackoverflow.com/tags/jhipster) and [Ionic](http://stackoverflow.com/tags/ionic-framework) tags on StackOverflow or join our [Gitter.im chat room](https://gitter.im/jhipster/generator-jhipster).

## <a name="issue"></a> Issues and Bugs

If you find a bug in the source code or a mistake in the documentation, you can help us by [submitting a ticket](https://opensource.guide/how-to-contribute/#opening-an-issue) to our [GitHub issues](https://github.com/oktadeveloper/generator-jhipster-ionic/issues). Even better, you can submit a pull request to the [Ionic for JHipster generator project](https://github.com/oktadeveloper/generator-jhipster-ionic).

**Please see the Submission Guidelines below**.

## <a name="feature"></a> Feature Requests

You can request a new feature by submitting a ticket to our [GitHub issues](https://github.com/oktadeveloper/generator-jhipster-ionic/issues). If you
would like to implement a new feature then consider what kind of change it is:

- **Major Changes** that you wish to contribute to the project should be discussed first. Please open a ticket which clearly states that it is a feature request in the title and explain clearly what you want to achieve in the description, and the JHipster team will discuss with you what should be done in that ticket. You can then start working on a Pull Request.
- **Small Changes** can be proposed without any discussion. Open up a ticket which clearly states that it is a feature request in the title. Explain your change in the description, and you can propose a Pull Request straight away.

## <a name="submit"></a> Submission Guidelines

### [Submitting an Issue](https://opensource.guide/how-to-contribute/#opening-an-issue)

Before you submit your issue search the [archive](https://github.com/oktadeveloper/generator-jhipster-ionic/issues?utf8=%E2%9C%93&q=is%3Aissue), maybe your question was already answered.

If your issue appears to be a bug, and has not been reported, open a new issue.
Help us to maximize the effort we can spend fixing issues and adding new
features, by not reporting duplicate issues. Providing the following information will increase the
chances of your issue being dealt with quickly:

- **Overview of the issue** - if an error is being thrown a stack trace helps
- **Motivation for or Use Case** - explain why this is a bug for you
- **Reproduce the error** - an unambiguous set of steps to reproduce the error. If you have a JavaScript error, maybe you can provide a live example with
  [JSFiddle](http://jsfiddle.net/)?
- **Related issues** - has a similar issue been reported before?
- **Suggest a Fix** - if you can't fix the bug yourself, perhaps you can point to what might be
  causing the problem (line of code or commit)
- **JHipster Version(s)** - is it a regression?
- **JHipster configuration, a `.yo-rc.json` file generated in the root folder** - this will help us to replicate the scenario, you can remove the rememberMe key.
- **Entity configuration(s) `entityName.json` files generated in the `.jhipster` directory** - if the error is during an entity creation or associated with a specific entity
- **Browsers and Operating System** - is this a problem with all browsers or only IE8?

You can use `jhipster info` to provide us the information we need.

Click [here](https://github.com/oktadeveloper/generator-jhipster-ionic/issues/new) to open a bug issue with a pre-filled template. For feature requests and enquiries you can use [this template][feature-template].

You can run `jhipster info` in your project folder to get most of the above required info.

Issues opened without any of these info will be **closed** without any explanation.

### [Submitting a Pull Request](https://opensource.guide/how-to-contribute/#opening-a-pull-request)

Before you submit your pull request consider the following guidelines:

- Search [GitHub](https://github.com/oktadeveloper/generator-jhipster-ionic/pulls?utf8=%E2%9C%93&q=is%3Apr) for an open or closed Pull Request
  that relates to your submission.
- If you want to modify the JHipster generator, read our [Generator development setup](#setup)
- Make your changes in a new git branch

  ```shell
  git checkout -b my-fix-branch master
  ```

- Create your patch, **including appropriate test cases**.
- Follow our [Coding Rules](#rules).
- Generate a new Ionic for JHipster project, and ensure that all tests pass

  ```shell
  yo jhipster-ionic <name>
  cd name && ionic test
  ```

- Test that the new project runs correctly:

  ```shell
  ionic serve
  ```

- Commit your changes using a descriptive commit message that follows our
  [commit message conventions](#commit-message-format).

  ```shell
  git commit -a
  ```

  Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files.

- Push your branch to GitHub:

  ```shell
  git push origin my-fix-branch
  ```

- In GitHub, send a pull request to `oktadeveloper/generator-jhipster-ionic:master`.
- If we suggest changes then

  - Make the required updates.
  - Re-run the JHipster tests on your sample generated project to ensure tests are still passing.
  - Rebase your branch and force push to your GitHub repository (this will update your Pull Request):

    ```shell
    git rebase master -i
    git push -f
    ```

That's it! Thank you for your contribution!

#### Resolving merge conflicts ("This branch has conflicts that must be resolved")

Sometimes your PR will have merge conflicts with the upstream repository's master branch. There are several ways to solve this but if not done correctly this can end up as a true nightmare. So here is one method that works quite well.

- First, fetch the latest information from the master

  ```shell
  git fetch upstream
  ```

- Rebase your branch against the upstream/master

  ```shell
  git rebase upstream/master
  ```

- Git will stop rebasing at the first merge conflict and indicate which file is in conflict. Edit the file, resolve the conflict then

  ```shell
  git add <the file that was in conflict>
  git rebase --continue
  ```

- The rebase will continue up to the next conflict. Repeat the previous step until all files are merged and the rebase ends successfully.
- Re-run the JHipster tests on your sample generated project to ensure tests are still passing.
- Force push to your GitHub repository (this will update your Pull Request)

  ```shell
  git push -f
  ```

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

- Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

  ```shell
  git push origin --delete my-fix-branch
  ```

- Check out the master branch:

  ```shell
  git checkout master -f
  ```

- Delete the local branch:

  ```shell
  git branch -D my-fix-branch
  ```

- Update your master with the latest upstream version:

  ```shell
  git pull --ff upstream master
  ```

## <a name="setup"></a> Generator development setup

Ionic for JHipster is a [JHipster Module](http://www.jhipster.tech/modules/creating-a-module/). You might want to follow the [Yeoman authoring documentation](http://yeoman.io/authoring/) in order to be able to run and test your changes.

Here are the most important steps.

### Fork the generator-jhipster-ionic project

Go to the [generator-jhipster-ionic project](https://github.com/oktadeveloper/generator-jhipster-ionic) and click on the "fork" button. You can then clone your own fork of the project, and start working on it.

[Please read the GitHub forking documentation for more information](https://help.github.com/articles/fork-a-repo)

### Set NPM/YARN to use the cloned project

In your cloned `generator-jhipster-ionic` project, type `npm link` or `yarn link` depending on the package manager you use.

This will do a symbolic link from the global `node_modules` version to point to this folder, so when you run `yo jhipster-ionic`, you will now use the development version of Ionic for JHipster.

For testing, you will want to generate an application, and there is a specific issue here: for each application, Ionic for JHipster installs a local version of itself. This is made to enable several applications to each use a specific Ionic for JHipster version (application A uses Ionic for JHipster 3.1.0, and application B uses Ionic for JHipster 3.2.0).

To overcome this you need to run `npm link generator-jhipster-ionic` or `yarn link generator-jhipster-ionic` on the generated project folder as well, so that the local version has a symbolic link to the development version of JHipster.

To put it in a nutshell, you need to:

1. run `npm link` or `yarn link` on the `generator-jhipster-ionic` project
2. run `npm link generator-jhipster-ionic` or `yarn link generator-jhipster-ionic` on the generated application folder (you need to do this for each application you create)

Now, running the `yo jhipster-ionic` command should use your specific Ionic for JHipster version. You can test it by making a small change in your cloned generator, and running again on an existing Ionic project:

```shell
yo jhipster-ionic:entity <name>
```

You should see your changes reflected in the generated project.

## <a name="rules"></a> Coding Rules

To ensure consistency throughout the source code, keep these rules in mind as you are working:

- All features or bug fixes **should be tested** by one or more tests.
- All files must follow the [.editorconfig file](http://editorconfig.org/) located at the root of the JHipster generator project. Please note that generated projects use the same `.editorconfig` file, so that both the generator and the generated projects share the same configuration.
- Java files **must be** formatted using [Intellij IDEA's code style](http://confluence.jetbrains.com/display/IntelliJIDEA/Code+Style+and+Formatting). Please note that JHipster committers have a free Intellij IDEA Ultimate Edition for developing the project.
- Generators JavaScript files **must follow** the eslint configuration defined at the project root, which is based on [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript).
- Web apps JavaScript files **must follow** [Google's JavaScript Style Guide](https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml).
- Typescript files **must follow** [Official Angular style guide](https://angular.io/styleguide).

Please ensure to run `npm run lint` and `npm test` on the project root before submitting a pull request. You can also run `npm run lint-fix` to fix some of the lint issues automatically.

## <a name="templates"></a> Template Guidelines

The template engine used by Yeoman is [EJS](http://ejs.co/), its syntax is fairly simple.

## <a name="commit"></a> Git Commit Guidelines

We have rules over how our git commit messages must be formatted. Please ensure to [squash](https://help.github.com/articles/about-git-rebase/#commands-available-while-rebasing) unnecessary commits so that your commit history is clean.

### <a name="commit-message-format"></a> Commit Message Format

Each commit message consists of a **header**, a **body** and a **footer**.

```
<header>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

Any line of the commit message cannot be longer 100 characters! This allows the message to be easier
to read on GitHub as well as in various git tools.

### Header

The Header contains a succinct description of the change:

- use the imperative, present tense: "change" not "changed" nor "changes"
- don't capitalize first letter
- no dot (.) at the end

### Body

If your change is simple, the Body is optional.

Just as in the Header, use the imperative, present tense: "change" not "changed" nor "changes".
The Body should include the motivation for the change and contrast this with previous behavior.

### Footer

The footer is the place to reference GitHub issues that this commit **Closes**.

You **must** use the [GitHub keywords](https://help.github.com/articles/closing-issues-via-commit-messages) for
automatically closing the issues referenced in your commit.

### Example

For example, here is a good commit message:

```
upgrade to JHipster 4.11.1

upgrade the required version of JHipster to be 4.11.1,
see http://www.jhipster.tech/2017/11/26/jhipster-release-4.11.1.html

Fix #1234
```

[feature-template]: https://github.com/oktadeveloper/generator-jhipster-ionic/issues/new?body=*%20**Overview%20of%20the%20request**%0A%0A%3C!--%20what%20is%20the%20query%20or%20request%20--%3E%0A%0A*%20**Motivation%20for%20or%20Use%20Case**%20%0A%0A%3C!--%20explain%20why%20this%20is%20a%20required%20for%20you%20--%3E%0A%0A%0A*%20**Browsers%20and%20Operating%20System**%20%0A%0A%3C!--%20is%20this%20a%20problem%20with%20all%20browsers%20or%20only%20IE8%3F%20--%3E%0A%0A%0A*%20**Related%20issues**%20%0A%0A%3C!--%20has%20a%20similar%20issue%20been%20reported%20before%3F%20--%3E%0A%0A*%20**Suggest%20a%20Fix**%20%0A%0A%3C!--%20if%20you%20can%27t%20fix%20this%20yourself%2C%20perhaps%20you%20can%20point%20to%20what%20might%20be%0A%20%20causing%20the%20problem%20(line%20of%20code%20or%20commit)%20--%3E
