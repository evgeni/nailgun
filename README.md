NailGun
=======

NailGun is a GPL-licensed Python library that facilitates easy usage of the
Satellite 6 API.

Why NailGun?
------------

NailGun exists to make working with the Satellite 6 API easier.

* Existing libraries, such as the Python
  [Requests](http://docs.python-requests.org/en/latest/) library, are
  general-purpose tools. As a result, client code can easily become excessively
  verbose. For example, see the `get_org_envs.py` script.
* The Satellite 6 API is not RESTful in its design.
* The Satellite 6 API is not consistent in its implementation. For example, see
  the "Payload Generation" section of [this blog
  post](http://www.ichimonji10.name/blog/4/) blog post.
* The Satellite 6 API contains bugs which are often long-lived. For example, it
  is impossible to definitively know whether a given activation key exists, due
  to [foreman bug #4638](http://projects.theforeman.org/issues/4638).

All of the above issues are compounded by the size of the Satellite 6 API. As of
this writing, there are 405 paths. This makes it tough to design compact and
elegant client code.

NailGun addresses these issues. NailGun is specialized, it has a consistent
design, it abstracts away many painful implementation details and it contains
workarounds for certain bugs. Why use a hammer when you can use a nail gun?

Scope and Limitations
---------------------

NailGun is not an officially supported product. NailGun is a Python-only
library, and integration with other languages such as Java or Ruby is not
currently a consideration. Although NailGun is developed with a broad audience
in mind, it targets [Robottelo](http://robottelo.readthedocs.org/en/latest/)
first and foremost.

Miscellany
----------

If you'd like to chat with a human, please join the #robottelo channel on the
[freenode](https://freenode.net/) IRC network.

For in-depth examples of how to use NailGun, see the Robottelo [source
code](https://github.com/SatelliteQE/robottelo), especially the
[`tests/foreman/api/`](https://github.com/SatelliteQE/robottelo/tree/master/tests/foreman/api).
directory For a glimpse into the design of NailGun, see [this blog
post](http://www.ichimonji10.name/blog/4/).

Contributions are encouraged. The easiest way to contribute is to submit a pull
request on GitHub, but patches are welcome no matter how they arrive. Please
adhere to the following guidelines:

* Lint your code with flake8 and pylint. The former linter must pass with zero
  warnings, and warnings from the latter linter should be minimized.
* All code must be documented, and use of Sphinx directives is encouraged.
* Unit tests are _very_ highly recommended.
* All typical commit guidelines apply:
  * Commits should not cause NailGun to break.
  * Commits should be small and coherent. One commit should address one issue.
  * Commits should have [good commit
    messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html).
  * [Rebasing](http://www.git-scm.com/book/en/v2/Git-Branching-Rebasing) is
    encouraged. Rebasing produces a much nicer commit history than merging.
* When in doubt, ask on IRC.
