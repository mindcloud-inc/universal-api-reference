# <img src="https://images.mindcloud.co/apps/icons/formspark-icon_1775838062115.png" alt="Formspark logo" width="28" height="28"> Formspark: Universal API

Formspark lets you send submissions to hosted form endpoints without running your own backend. This app wraps Formspark's documented public form submission surface, including AJAX submissions, redirect controls, feedback-page customization, reply routing, spam-protection fields, file-link submissions, and structured payload patterns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formspark/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://formspark.io
- **Vendor API docs:** https://documentation.formspark.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Submit Form JSON](actions/submit-form-json.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "your-form-id"
}'
```

## Actions (28)

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Submit Form JSON](actions/submit-form-json.md) | POST | Creates a Formspark form submission from a JSON payload. |
| [Submit Form URL Query Payload](actions/submit-form-url-query-payload.md) | POST | Creates a Formspark form submission from query parameters. |
| [Submit Form With Array Fields](actions/submit-form-with-array-fields.md) | POST | Creates a Formspark form submission with array fields. |
| [Submit Form With Botpoison](actions/submit-form-with-botpoison.md) | POST | Creates a Formspark form submission with Botpoison validation. |
| [Submit Form With Checkbox Fields](actions/submit-form-with-checkbox-fields.md) | POST | Creates a Formspark form submission with checkbox fields. |
| [Submit Form With Custom Honeypot Field](actions/submit-form-with-custom-honeypot-field.md) | POST | Creates a Formspark form submission with a custom honeypot field. |
| [Submit Form With Direct Reply](actions/submit-form-with-direct-reply.md) | POST | Creates a Formspark form submission with direct reply settings. |
| [Submit Form With Error Redirect](actions/submit-form-with-error-redirect.md) | POST | Creates a Formspark form submission with success and error redirects. |
| [Submit Form With Extended UTM Parameters](actions/submit-form-with-extended-utm-parameters.md) | POST | Creates a Formspark form submission with extended UTM parameters. |
| [Submit Form With Feedback Messages](actions/submit-form-with-feedback-messages.md) | POST | Creates a Formspark form submission with custom feedback messages. |
| [Submit Form With Feedback Page](actions/submit-form-with-feedback-page.md) | POST | Creates a Formspark form submission with feedback page settings. |
| [Submit Form With Gotcha Honeypot](actions/submit-form-with-gotcha-honeypot.md) | POST | Creates a Formspark form submission with a gotcha honeypot field. |
| [Submit Form With hCaptcha](actions/submit-form-with-hcaptcha.md) | POST | Creates a Formspark form submission with hCaptcha validation. |
| [Submit Form With Hidden Metadata Field](actions/submit-form-with-hidden-metadata-field.md) | POST | Creates a Formspark form submission with a hidden metadata field. |
| [Submit Form With Honeypot](actions/submit-form-with-honeypot.md) | POST | Creates a Formspark form submission with a honeypot field. |
| [Submit Form With Mail Reply Alias](actions/submit-form-with-mail-reply-alias.md) | POST | Creates a Formspark form submission using the mail reply alias. |
| [Submit Form With Multi Select](actions/submit-form-with-multi-select.md) | POST | Creates a Formspark form submission with multiple selected values. |
| [Submit Form With Nested Email Object](actions/submit-form-with-nested-email-object.md) | POST | Creates a Formspark form submission with nested email settings. |
| [Submit Form With Notification Email](actions/submit-form-with-notification-email.md) | POST | Creates a Formspark form submission with notification email settings. |
| [Submit Form With Object Fields](actions/submit-form-with-object-fields.md) | POST | Creates a Formspark form submission with object fields. |
| [Submit Form With Radio Choice](actions/submit-form-with-radio-choice.md) | POST | Creates a Formspark form submission with a radio choice. |
| [Submit Form With reCAPTCHA](actions/submit-form-with-recaptcha.md) | POST | Creates a Formspark form submission with reCAPTCHA validation. |
| [Submit Form With Redirect](actions/submit-form-with-redirect.md) | POST | Creates a Formspark form submission with redirect settings. |
| [Submit Form With ReplyTo Alias](actions/submit-form-with-replyto-alias.md) | POST | Creates a Formspark form submission using the ReplyTo alias. |
| [Submit Form With Single Select](actions/submit-form-with-single-select.md) | POST | Creates a Formspark form submission with a single select value. |
| [Submit Form With Turnstile](actions/submit-form-with-turnstile.md) | POST | Creates a Formspark form submission with Turnstile validation. |
| [Submit Form With Uploadcare File Link](actions/submit-form-with-uploadcare-file-link.md) | POST | Creates a Formspark form submission with an Uploadcare file URL. |
| [Submit Form With UTM Parameters](actions/submit-form-with-utm-parameters.md) | POST | Creates a Formspark form submission with UTM tracking parameters. |

