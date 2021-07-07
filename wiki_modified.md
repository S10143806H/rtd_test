Table of Content
================

- [Table of Content](#table-of-content)
- [Code Acceptance](#code-acceptance)
- [Coding Style](#coding-style)
  - [Naming Conventions](#naming-conventions)
      - [Classes](#classes)
      - [Functions](#functions)
- [Contribution Guideline](#contribution-guideline)
  - [GitHub Pull Requests](#github-pull-requests)
- [Reporting Bugs](#reporting-bugs)

<br>

----

> :warning: The Ameba Arduino / SDK / MicroPython codebase are hosted on GitHub, you can submit new features or bug fixes using ``Pull Request`` on Github. 
> 
> Before you do so, please read the [**Coding Style**](#coding-style) and [**Contribution Guideline**](#contribution-guideline) section.

<br>


Test of GIF
============
![Alt Text](https://media.giphy.com/media/vFKqnCdLPNOKc/giphy.gif)



Code Acceptance
===============

Once submit your ``Pull Request``, our developers will take a look and comment on the ``Pull Request``. If all is well and acceptable, your code will be ready for merging into the central development branch.

Coding Style
=============

Ameba Coding Style mostly adopt from Mbed OS. Whether you're writing new code or fixing bugs in existing code, please follow the Ameba coding style.

Ameba follows the [K&R style -- Variant: 1TBS](https://en.wikipedia.org/wiki/Indent_style#K.26R_style), with a few exceptions，

* Indentation - four spaces. Please do not use tabs.
* Braces - K&R style. One true brace style (1TBS) 
* One line per statement.
* Each line preferably has at most 120 characters.
* Space after statements of type `if` , `while` , `for` , `switch` . The same applies to operators (like, `+`, '=' and `*` ) and the ternary operator ( `?` and `:` ).
* For pointers or references, the symbols `*` or `&` are adjacent to a type ( `analogin_t* obj` . `analogin_t& obj` ). 
* Empty lines should have no trailing spaces.
* Use capital letters for macros.
* Preprocessor macro starts at the beginning of a new line; the code inside is indented according to the code above it.

Naming Conventions
------------------

#### Classes

* Begin with a capital letter, and each word within a class also begins with a capital letter (AnalogIn, BusInOut).
* Private members start with an underscore: `__User defined types (typedef)))` .


#### Functions

* Use lower case letters
* Words separated by a capital letter of the subsequent work (readDir, getRootPath).

<br>
<br>
<br>

----


Contribution Guideline
======================

Before contributing an enhancement (for example, a new feature or new port), please [discuss it on the forums](https://forum.amebaiot.com/) or on the [Facebook group](https://www.facebook.com/groups/AmebaIoT) to avoid duplication of work, as we or others might be working on a related feature.

We can only accept contributions through GitHub if you create a ``Pull Request`` from forked versions of our repositories. This allows us to review the contributions in an easy-to-use and reliable way, under public scrutiny.

Please create separate ``Pull Requests`` for each topic; each ``Pull Request`` needs a clear unity of purpose. In particular, separate code formatting and style changes from functional changes. This makes each ``Pull Request``’s true contribution clearer, so review is quicker and easier.

Contribution items ``Pull Requested`` to Ameba's GitHub repository can be categorized as:
1. Hardware projects that involved with adding extra hardware peripherals
2. Pure software projects

For the contributed items that requries extra hardware peripherals, the project will be saved as a ".zip" zipped library that stores in the file path below: 
https://github.com/ambiot/ambd_arduino/tree/master/Arduino_zip_libraries

For the software-based projects, will be placed in a sepearte file path: https://github.com/ambiot/ambd_arduino/tree/master/Arduino_package/hardware that fully supported by offcial. 

GitHub Pull Requests
---------------------

``Pull Request`` on GitHub have to meet the following requirements to keep the code and commit history clean:

* Commits must always contain a proper description of their content. Start with a concise and sensible one-line description. Then, elaborate on reasoning of the choices made, descriptions for reviewers and other information that might otherwise be lost.
* You should always write commits that allow publication. They must not contain confidential information, references to private documents, links to intranet locations or rude language.
* Because we use GitHub, special commit tags that other projects may use, such as “Reviewed-by”, or “Signed-off-by”, are redundant and should be omitted. GitHub tracks who reviewed what and when.
* All new features and enhancements require documentation, tests and user guides for us to accept them. Please link each ``pull request`` to all relevant documentation and test ``pull requests``.
* Avoid merging commits. (Always rebase when possible)
* Avoid force pushing when making review changes, unless you're cleaning up your branch's history once the changes have been approved.
* Comment in the ``pull request`` on every change (rebase or new commits). This helps reviewers to be up to date with changes
* Smaller ``pull requests`` are easier to review and faster to integrate. Use dependencies – split your work by ``pull request`` type or functional changes. To add a third-party driver, send it in a separate ``pull request``, and add it as a dependency to your ``pull request``.

  <br>
  See example here:

      Update early access SDK 3.0.9-build20210408

      Feature:
      - support board RTL8720DN_BW16
      - update Eink lib
      API Updates:
      - pre support Microsoft Azure IoT cloud
      -- enable "strnlen" from rom
      -- add "#define yield" for compilation
      - update SPI, I2C, Fatfs, Audiocodec and UART for RTL8720DN_BW16
      Misc:
      - add RTL8720DN_BW16 frizting folder


If commits do not follow the above guidelines, we may request that you modify the commit history (often to add more details to address *what* and *why* rather than *how* ).

Reporting Bugs
================

You can submit Ameba bugs directly on [GitHub](https://github.com/ambiot). Please submit questions or enhancement requests on the [ forums](https://forum.amebaiot.com/) or on the [Facebook group](https://www.facebook.com/groups/AmebaIoT)

The bug report should be reproducible (fails for others) and specific (where and how it fails). We will close insufficient bug reports.
