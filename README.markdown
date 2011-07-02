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

	type User struct {
			ID string // The user's ID, represented as an email in the current system.
			// contains filtered or unexported fields
	}

### func Get(c http.ResponseWriter, r *http.Request) (u *User, err os.Error)

### func GetExisting(r *http.Request) (u *User, err os.Error)

### func (u *User) Get(key string) string

### func (u *User) Set(key string, val string)

### func (u *User) Load() (err os.Error)

### func (u *User) Save() os.Error