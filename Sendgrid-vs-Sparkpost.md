This is an actual comparison between Sendgrid and Sparpost, after having actually used both for transactional emails, albeit with a small user base. No marketing talk here; just a developer-focused comparison.

# Sendgrid

Pros
+ analytics for recipient geography, email clients & devices, mailbox, and browser type
  ![mailbox provider](https://user-images.githubusercontent.com/33569/80805619-a3926d00-8c0c-11ea-9a1d-8a6b3dcf5e56.png)
  ![geography](https://user-images.githubusercontent.com/33569/80818225-e6613e80-8c26-11ea-9140-6ea3b6284826.png)
+ drag'n'drop visual email template designer (see limitations and issues below)
+ can have multiple versions for a given template, and marking one as "active" for use

Cons
- No [CSS inlining](https://github.com/sendgrid/sendgrid-nodejs/issues/199#issuecomment-621934265)
- Misleading status responses. When sending and email and the template fails to compile, the result is "success".
- [Status response doesn't include anything useful](https://github.com/sendgrid/sendgrid-nodejs/issues/1109).
- [Vague, unhelpful, error messages](https://github.com/sendgrid/docs/issues/5963)
- Slower web app than Sparkpost
- Disjointed support, with one Twilio team member not bothering to re-file a bug report to the correct repo, but instead [asking the bug reporter to do even more work](https://github.com/sendgrid/sendgrid-nodejs/issues/1096#issuecomment-615265177)
- [Can't schedule emails more than 72 hours in advance](https://github.com/sendgrid/sendgrid-nodejs/issues/166#issuecomment-255521853).
- The visual email template designer doesn't allow customizing the social media module, which includes a fixed set of social media links. It appears imposible to add, say, a Discord link.
- The email Activity doesn't show the body of the sent emails.
- Previously [confusing API, until a random contributor rewrote it](https://github.com/sendgrid/sendgrid-nodejs/pull/378#issuecomment-291633854) in 2017

Free plan
- 100 emails/day

# Sparkpost

Pros:
* AMPHTML support, for [dynamic emails](https://amp.dev/about/email/)
* [CSS inlining](https://www.sparkpost.com/blog/automatic-css-inlining-sparkpost/), critical for Protonmail and possibly other providers
* [Much more powerful template language](https://developers.sparkpost.com/api/template-language/) than Sendgrid's crippled Handlebars (which is already [handicapped](https://stackoverflow.com/questions/8853396/logical-operator-in-a-handlebars-js-if-conditional#comment41160929_9405113))
* Sending an email returns a useful ID in the response

Cons:
- no analytics about recipient geography or email client time; only [opens/rejections/bounces](https://www.sparkpost.com/docs/reporting/signals-analytics/)
- Plain HTML template editor, with an [odd page about it](https://www.sparkpost.com/template-editor/) ([2020-May-01 mirror](https://web.archive.org/web/20200501060248/https://www.sparkpost.com/template-editor/)). Instead, they [recommend](https://www.sparkpost.com/blog/topol-html-email-templates/) a separate tool for visually designing emails, [Topol](https://topol.io/)
- [Awkward](https://github.com/SparkPost/developers.sparkpost.com/issues/376) error message display when compiling templates
- [Template errors are listed backwards](https://github.com/SparkPost/developers.sparkpost.com/issues/377)
- [Template editor has no undo](https://github.com/SparkPost/developers.sparkpost.com/issues/378)
- [Can't schedule emails more than 72 hours in advance](https://developers.sparkpost.com/api/transmissions/#transmissions-post-schedule-a-transmission).
- The email Activity doesn't show the body of the sent emails.

Free plan:
- 100 emails/day
