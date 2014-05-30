## Contributing

This project follows the [git flow](http://nvie.com/posts/a-successful-git-branching-model/) branching model of product development.

### <a name="code-style"></a> Code Style

We generally adhere to the [GitHub Style Guide](https://github.com/styleguide/).

Spaces should be used instead of tabs, and the tab width should be set to 2 spaces.  No spaces at the end of lines.

### <a name="commit-messages"></a> Commit Messages

Treat commit messages as an email message that describes what you changed and why.

The first line of the commit log must be treated as as an email
subject line.  It must be strictly no greater than 50 characters long.
The subject must stand on its own and not only make external
references such as to relevant bug numbers.

The second line must be blank.

The third line begins the body of the commit message (one or more
paragraphs) describing the details of the commit.  Paragraphs are each
separated by a blank line.  Paragraphs must be word wrapped to be no
longer than 76 characters.

The last part of the commit log should contain all "external
references", such as which issues were fixed.

## <a name="submit"></a> Submission Guidelines

### Submitting a Pull Request
Before you submit your pull request consider the following guidelines:

* Search [GitHub](https://github.com/18F/18f.gsa.gov/pulls) for an open or closed Pull Request that relates to your submission. You don't want to duplicate effort.
* Make your changes in a new git branch

    ```shell
    git checkout -b my-fix-branch devel
    ```

* Create your patch, **including appropriate test cases**.
* Follow our [Code Style](#code-style).
* Commit your changes using a descriptive commit message that follows our
  [commit message conventions](#commit-messages). Adherence to the [commit message conventions](#commit-messages)
  is required to assist in generating release notes.

    ```shell
    git commit -a
    ```
  Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files -- **use at your own risk!**

* Push your branch to GitHub:

    ```shell
    git push origin my-fix-branch
    ```

* In GitHub, send a pull request to `18f.gsa.gov:devel`.
* If we suggest changes to the pull request after submitted, then:
  * Make the required updates.
  * Re-run the necessary minification commands.

That's it! Thank you for your contribution!

### Submitting an Issue
Before you submit your issue, please [search the archive](https://github.com/18F/18f.gsa.gov/issues?direction=desc&sort=updated&state=closed). Maybe your question was already answered.

If your issue appears to be a bug, and hasn't been reported, open a new issue.
Help us to maximize the effort we can spend fixing issues and adding new
features by not reporting duplicate issues.  Providing the following information will increase the
chances of your issue being dealt with quickly:

* **Overview of the issue** - if an error is being thrown a non-minified stack trace helps
* **Motivation for or Use Case** - explain why this is a bug for you
* **Browsers and Operating System** - is this a problem with all browsers or only IE8?
* **Reproduce the error** - provide a live example, screenshot, and/or a unambiguous set of steps. The more the better.
* **Related issues** - has a similar issue been reported before?  Reference the related issues in the description.
* **Suggest a Fix** - if you can't fix the bug yourself, perhaps you can point to what might be causing the problem (line of code or commit).  If you're requesting a feature, describe how the feature might work to resolve the user story.

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete my-fix-branch
    ```

* Check out the devel branch:

    ```shell
    git checkout devel -f
    ```

* Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```

* Update your devel with the latest upstream version:

    ```shell
    git pull --ff upstream devel
    ```
