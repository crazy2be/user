User Settings Storage Package
=============================

A simple package that allows persistent server-side storage of user settings and data. Similar to the session package (http://github.com/crazy2be/session), but settings persist between sessions, and are associated with a particular user rather than a particular session.

Getting Started
---------------

Install:

	goinstall github.com/crazy2be/user

Import:

	import "github.com/crazy2be/user"

Use:

	u, err := user.Get(c, r)

	if err != nil {
		template.Error500(err)
		return
	}

	showWelcomeBanner := u.Get("show-welcome-banner")


Functions
---------

See http://gopkgdoc.appspot.com/pkg/github.com/crazy2be/user for the full function reference.