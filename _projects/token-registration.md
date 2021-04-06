---
name: Token Authenticated Registration
desc: Let server admins allow people with a valid token to register, but no-one else.
# add a short one line description of your project
requirements:
# Student requirements:
difficulty: medium (?)
issues:
# Related issues (if any)  to this project.
mentors:
# First person in contact; mentors may change before project starts.
initiatives:
 - GSoC
tags:
# Different technologies needed
---

#### Description

At the moment, Matrix homeserver administrators must choose between allowing
registrations from everyone, or closing registrations completely. Some admins
would like another option, which would allow certain authenticated people to
register as usual through Matrix clients, but deny anyone else.

There are existing tools which tackle this problem, such as
[matrix-registration](https://github.com/ZerataX/matrix-registration/),
however they require extra effort to set-up and maintain, and do not provide
the unified user experience that registration through a Matrix client does.
This project would integrate token authenticated registration into the Matrix
specification and implement it in a server and a client.

#### Milestones

##### GSoC CODING STARTS

* Define a new authentication type to use with the
[User-Interactive Authentication API](https://matrix.org/docs/spec/client_server/r0.6.1#user-interactive-authentication-api)

##### GSoC MIDTERM

* Implement the generation and management of registration tokens in a Matrix
  server.
* Add an option to a server which requires a valid token in order for a new
  account to be registered.

##### GSoC FINAL

* Implement the ability to submit a token while registering in a Matrix client.
* Add a fallback for clients which do not support token authenticated
  registration.
