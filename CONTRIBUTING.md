# Contributing to CoreUI

Looking to contribute something to CoreUI? **Here's how you can help.**

Please take a moment to review this document in order to make the contribution process easy and effective for everyone involved.

Following these guidelines helps to communicate that you respect the time of the developers managing and developing this open source project. In return, they should reciprocate that respect in addressing your issue or assessing
patches and features.

## Using the issue tracker

The [issue tracker](https://github.com/coreui/coreui/issues) is
the preferred channel for [bug reports](#bug-reports), [features requests](#feature-requests)
and [submitting pull requests](#pull-requests), but please respect the following
restrictions:

* Please **do not** use the issue tracker for personal support requests.

* Please **do not** post comments consisting solely of "+1" or ":thumbsup:".
  Use [GitHub's "reactions" feature](https://github.com/blog/2119-add-reactions-to-pull-requests-issues-and-comments)
  instead.

<!-- ## Issues and labels

Our bug tracker utilizes several labels to help organize and identify issues. Here's what they represent and how we use them:

- `browser bug` - Issues that are reported to us, but actually are the result of a browser-specific bug. These are diagnosed with reduced test cases and result in an issue opened on that browser's own bug tracker.
- `confirmed` - Issues that have been confirmed with a reduced test case and identify a bug in Bootstrap.
- `css` - Issues stemming from our compiled CSS or source Less/Sass files.
- `customizer` - Issues with our web-based Customizer.
- `docs` - Issues for improving or updating our documentation.
- `examples` - Issues involving the example templates included in our docs.
- `feature` - Issues asking for a new feature to be added, or an existing one to be extended or modified. New features require a minor version bump (e.g., `v3.0.0` to `v3.1.0`).
- `grunt` - Issues with our included JavaScript-based Gruntfile, which is used to run all our tests, concatenate and compile source files, and more.
- `help wanted` - Issues we need or would love help from the community to resolve.
- `js` - Issues stemming from our compiled or source JavaScript files.
- `meta` - Issues with the project itself or our GitHub repository.

For a complete look at our labels, see the [project labels page](https://github.com/twbs/bootstrap/labels). -->


## Bug reports

A bug is a _demonstrable problem_ that is caused by the code in the repository.
Good bug reports are extremely helpful, so thanks!

Guidelines for bug reports:

0. **Validate and lint your code** &mdash; to ensure your problem isn't caused by a simple error in your own code.

1. **Use the GitHub issue search** &mdash; check if the issue has already been reported.

2. **Check if the issue has been fixed** &mdash; try to reproduce it using the latest `master` or development branch in the repository.

3. **Isolate the problem** &mdash; ideally create a [reduced test case](https://css-tricks.com/reduced-test-cases/) and a live example. [This JS Bin](http://jsbin.com/lefey/1/edit?html,output) is a helpful template.


A good bug report shouldn't leave others needing to chase you up for more
information. Please try to be as detailed as possible in your report. What is
your environment? What steps will reproduce the issue? What browser(s) and OS
experience the problem? Do other browsers show the bug differently? What
would you expect to be the outcome? All these details will help people to fix
any potential bugs.

Example:

> Short and descriptive example bug report title
>
> A summary of the issue and the browser/OS environment in which it occurs. If
> suitable, include the steps required to reproduce the bug.
>
> 1. This is the first step
> 2. This is the second step
> 3. Further steps, etc.
>
> `<url>` - a link to the reduced test case
>
> Any other information you want to share that is relevant to the issue being
> reported. This might include the lines of code that you have identified as
> causing the bug, and potential solutions (and your opinions on their
> merits).

## Feature requests

Feature requests are welcome. Before opening a feature request, please take a moment to find out whether your idea
fits with the scope and aims of the project. It's up to *you* to make a strong
case to convince the project's developers of the merits of this feature. Please
provide as much detail and context as possible.


## Pull requests

Good pull requests—patches, improvements, new features—are a fantastic
help. They should remain focused in scope and avoid containing unrelated
commits.

**Please ask first** before embarking on any significant pull request (e.g.
implementing features, refactoring code, porting to a different language),
otherwise you risk spending a lot of time working on something that the
project's developers might not want to merge into the project.

Adhering to the following process is the best way to get your work
included in the project:

1. [Fork](https://help.github.com/fork-a-repo/) the project, clone your fork,
   and configure the remotes:

   ```bash
   # Clone your fork of the repo into the current directory
   git clone https://github.com/<your-username>/coreui.git
   # Navigate to the newly cloned directory
   cd coreui
   # Assign the original repo to a remote called "upstream"
   git remote add upstream https://github.com/coreui/coreui.git
   ```

2. If you cloned a while ago, get the latest changes from upstream:

   ```bash
   git checkout master
   git pull upstream master
   ```

3. Create a new topic branch (off the main project development branch) to
   contain your feature, change, or fix:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Commit your changes in logical chunks. Please adhere to these [git commit
   message guidelines](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
   or your code is unlikely to be merged into the main project. Use Git's
   [interactive rebase](https://help.github.com/articles/interactive-rebase)
   feature to tidy up your commits before making them public.

5. Locally merge (or rebase) the upstream development branch into your topic branch:

   ```bash
   git pull [--rebase] upstream master
   ```

6. Push your topic branch up to your fork:

   ```bash
   git push origin <topic-branch-name>
   ```

7. [Open a Pull Request](https://help.github.com/articles/using-pull-requests/)
    with a clear title and description against the `master` branch.

**IMPORTANT**: By submitting a patch, you agree to allow the project owners to
license your work under the terms of the [MIT License](LICENSE) (if it
includes code changes) and under the terms of the
[Creative Commons Attribution 3.0 Unported License](docs/LICENSE)
(if it includes documentation changes).


## Code guidelines

### HTML

[Adhere to the Code Guide.](http://codeguide.co/#html)

- Use tags and elements appropriate for an HTML5 doctype (e.g., self-closing tags).
- Use CDNs and HTTPS for third-party JS when possible. We don't use protocol-relative URLs in this case because they break when viewing the page locally via `file://`.
- Use [WAI-ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA) attributes in documentation examples to promote accessibility.

### CSS

[Adhere to the Code Guide.](http://codeguide.co/#css)

- When feasible, default color palettes should comply with [WCAG color contrast guidelines](http://www.w3.org/TR/WCAG20/#visual-audio-contrast).
- Except in rare cases, don't remove default `:focus` styles (via e.g. `outline: none;`) without providing alternative styles. See [this A11Y Project post](http://a11yproject.com/posts/never-remove-css-outlines) for more details.

### JS

- No semicolons (in client-side JS)
- 2 spaces (no tabs)
- strict mode
- "Attractive"
- Don't use [jQuery event alias convenience methods](https://github.com/jquery/jquery/blob/master/src/event/alias.js) (such as `$().focus()`). Instead, use [`$().trigger(eventType, ...)`](http://api.jquery.com/trigger/) or [`$().on(eventType, ...)`](http://api.jquery.com/on/), depending on whether you're firing an event or listening for an event. (For example, `$().trigger('focus')` or `$().on('focus', function (event) { /* handle focus event */ })`) We do this to be compatible with custom builds of jQuery where the event aliases module has been excluded.

## License

By contributing your code, you agree to license your contribution under the [MIT License](LICENSE).
By contributing to the documentation, you agree to license your contribution under the [Creative Commons Attribution 3.0 Unported License](docs/LICENSE).