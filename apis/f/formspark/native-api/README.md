# Formspark: Native API Reference

A consolidated summary of Formspark's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://documentation.formspark.io
- **API base URL:** `https://submit-form.com/`

## Authentication

### No Authentication

Formspark form submission endpoints do not require app-level credentials. Provide the target form ID in the action arguments and, when the form has anti-spam enabled, pass the documented anti-spam response field expected by that form.

This API does not require request authentication.

[Official authentication documentation](https://documentation.formspark.io/setup/installation.html)

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Submit Form JSON](actions/submit-form-json.md) | `POST :formId` | [docs](https://documentation.formspark.io/examples/ajax.html) |
| [Submit Form URL Query Payload](actions/submit-form-url-query-payload.md) | `POST :formId` | [docs](https://documentation.formspark.io/examples/ajax.html) |
| [Submit Form With Array Fields](actions/submit-form-with-array-fields.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/arrays-and-objects.html) |
| [Submit Form With Botpoison](actions/submit-form-with-botpoison.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/spam-protection.html) |
| [Submit Form With Checkbox Fields](actions/submit-form-with-checkbox-fields.md) | `POST :formId` | [docs](https://documentation.formspark.io/html-form/special-input-types.html) |
| [Submit Form With Custom Honeypot Field](actions/submit-form-with-custom-honeypot-field.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/spam-protection.html) |
| [Submit Form With Direct Reply](actions/submit-form-with-direct-reply.md) | `POST :formId` | [docs](https://documentation.formspark.io/customization/direct-replies.html) |
| [Submit Form With Error Redirect](actions/submit-form-with-error-redirect.md) | `POST :formId` | [docs](https://documentation.formspark.io/customization/redirection.html) |
| [Submit Form With Extended UTM Parameters](actions/submit-form-with-extended-utm-parameters.md) | `POST :formId` | [docs](https://documentation.formspark.io/integration/utm-parameters.html) |
| [Submit Form With Feedback Messages](actions/submit-form-with-feedback-messages.md) | `POST :formId` | [docs](https://documentation.formspark.io/customization/feedback-page.html) |
| [Submit Form With Feedback Page](actions/submit-form-with-feedback-page.md) | `POST :formId` | [docs](https://documentation.formspark.io/customization/feedback-page.html) |
| [Submit Form With Gotcha Honeypot](actions/submit-form-with-gotcha-honeypot.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/spam-protection.html) |
| [Submit Form With hCaptcha](actions/submit-form-with-hcaptcha.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/spam-protection.html) |
| [Submit Form With Hidden Metadata Field](actions/submit-form-with-hidden-metadata-field.md) | `POST :formId` | [docs](https://documentation.formspark.io/html-form/special-input-types.html) |
| [Submit Form With Honeypot](actions/submit-form-with-honeypot.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/spam-protection.html) |
| [Submit Form With Mail Reply Alias](actions/submit-form-with-mail-reply-alias.md) | `POST :formId` | [docs](https://documentation.formspark.io/customization/direct-replies.html) |
| [Submit Form With Multi Select](actions/submit-form-with-multi-select.md) | `POST :formId` | [docs](https://documentation.formspark.io/html-form/drop-down-list.html) |
| [Submit Form With Nested Email Object](actions/submit-form-with-nested-email-object.md) | `POST :formId` | [docs](https://documentation.formspark.io/examples/ajax.html) |
| [Submit Form With Notification Email](actions/submit-form-with-notification-email.md) | `POST :formId` | [docs](https://documentation.formspark.io/customization/notification-email.html) |
| [Submit Form With Object Fields](actions/submit-form-with-object-fields.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/arrays-and-objects.html) |
| [Submit Form With Radio Choice](actions/submit-form-with-radio-choice.md) | `POST :formId` | [docs](https://documentation.formspark.io/html-form/special-input-types.html) |
| [Submit Form With reCAPTCHA](actions/submit-form-with-recaptcha.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/spam-protection.html) |
| [Submit Form With Redirect](actions/submit-form-with-redirect.md) | `POST :formId` | [docs](https://documentation.formspark.io/customization/redirection.html) |
| [Submit Form With ReplyTo Alias](actions/submit-form-with-replyto-alias.md) | `POST :formId` | [docs](https://documentation.formspark.io/customization/direct-replies.html) |
| [Submit Form With Single Select](actions/submit-form-with-single-select.md) | `POST :formId` | [docs](https://documentation.formspark.io/html-form/drop-down-list.html) |
| [Submit Form With Turnstile](actions/submit-form-with-turnstile.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/spam-protection.html) |
| [Submit Form With Uploadcare File Link](actions/submit-form-with-uploadcare-file-link.md) | `POST :formId` | [docs](https://documentation.formspark.io/setup/file-uploads.html) |
| [Submit Form With UTM Parameters](actions/submit-form-with-utm-parameters.md) | `POST :formId` | [docs](https://documentation.formspark.io/integration/utm-parameters.html) |
