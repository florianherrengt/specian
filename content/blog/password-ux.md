---
title: "A better password input field"
date: 2020-06-09T00:00:00+00:00
image: images/blog/password-ux.jpg
summary: "Enforce strong passwords without degrading the user experience."
---

### Complexity requirements are useless

First of all, let's have a look at some statistics:

- 77% of passwords containing a single digit append it to the end of their password. 10% of the time, it will be a "1".
- 35% of passwords requiring a capital letter will capitalize the first letter.
- 89% of 7-character long alpha strings can be targeted by either capitalizing the first character or capitalizing the whole string.
- 61% of passwords are the exact length of the minimum length set in the password policy.
- Common substitutions (a = @, i = !, s = \$) are baked into password cracking rule-sets.

### Creating a strong password

- Think "passphrase" intead of "password". Five random words separated by special characters is hard for computers but still easy to remember.
- Avoid "password walking", password with adjacent keyboard characters (e.g. "qwerty", "asdfghjkl", "zxcvbnm1234")
- At the very least, your e-mail password should be extremely strong and unique.
- Ideally, you should be using a different password for every website. Find creative ways to include the name of the website.
- Best of all, use a password manager. We are big fans of [Bitwarden](https://bitwarden.com/).
- SMS-based two-factor authentication (2FA) is better than nothing but is vastly inferior to other forms of 2FA and MFA.
- Use a hardware key. [Solokeys](https://solokeys.com) are amazing. You plug it to your computer and your browser will ask you to press the button to log in.

### Product UX

How can we create a good user experience and enforce strong passwords?

- Don't Enforce complexity. As we saw earlier, complexity requirements don't increase password strengh. They only reduce the user experience.
- Don't make passwords expire. Password expiration has a negative impact on usability. Users change their passwords in predictable patterns (password1 -> password2 -> password3). Only require a password change if it has been compromised.
- Don't block copy/paste. Some products prevent users from pasting passwords. They want to force their users to type their password regularly so they don't forget it. But it comes at a significant cost. They can't use their password manager, the most secure option by far.

Odds are that you will annoy your users more than you will help them.

- Do respect semantics and standard practices. Name your field "password", not "user_password" or "app_pwd".
- Do check user passwords against a list of common or compromised passwords.
- Do enforce 2FA on sign up.
- Do provide the "Remember me" option.
- Do reduce sessions' lifespan. But renew it with each session. Users will be logged out if they don't use the app within x days.

### Read more and sources

[The father of password rules is sorry for wasting your time](https://specopssoft.com/blog/father-password-rules-sorry-wasting-time/)

[Testing Metrics for Password Creation Policies by Attacking Large Sets of Revealed Passwords](http://www.cs.umd.edu/~jkatz/security/downloads/passwords_revealed-weir.pdf)

[Beyond Password Length and Complexity](https://resources.infosecinstitute.com/beyond-password-length-complexity/)

[GitHub accounts targeted in password reuse attack](https://techcrunch.com/2016/06/16/github-accounts-targeted-in-password-reuse-attack/)

[Why you should use a password manager](https://nakedsecurity.sophos.com/2016/07/19/why-you-should-use-a-password-manager/)
