# Create SignRequest with SignRequest

## Endpoint

- **Method:** `POST`
- **Path:** `/signrequests/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [Create SignRequest](https://signrequest.com/api/v1/docs/#operation/signrequests_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `string` | yes | Document URL returned by the SignRequest documents API |
| `signers[]` | body | `array<object>` | yes | Signers to include on the SignRequest |
| `signers[].email` | body | `string` | yes | Signer email address Maximum length: 255. |
| `from_email` | body | `string` | no | Validated email address of the user sending the SignRequest Maximum length: 255. |
| `subject` | body | `string` | no | Subject of the SignRequest email Maximum length: 512. |
| `message` | body | `string` | no | Message to include in the SignRequest email |
| `who` | body | `list<string>` | no | Who needs to sign: only me, me and others, or only others Accepted values: `m`, `mo`, `o`. |
| `disable_emails` | body | `boolean` | no | Disable SignRequest status emails and signed-document emails |
| `send_reminders` | body | `boolean` | no | Automatically remind signers to sign |
| `from_email_name` | body | `string` | no | Name used in the From email header Maximum length: 255. |
| `first_name` | body | `string` | no | Signer first name Maximum length: 255. |
| `last_name` | body | `string` | no | Signer last name Maximum length: 255. |
| `signers[].order` | body | `number` | no | Signer order in the signing flow |
| `signers[].language` | body | `list<string>` | no | Signer language Accepted values: `da`, `de`, `en`, `en-gb`, `es`, `fi`, `fr`, `he`, `hu`, `it`, `ja`, `nl`, `no`, `pl`, `pt`, `ru`, `sv`. |
| `force_language` | body | `boolean` | no | Force the selected signer language |
| `needs_to_sign` | body | `boolean` | no | Whether the signer must sign the document |
| `approve_only` | body | `boolean` | no | Require approval without adding a signature |
| `notify_only` | body | `boolean` | no | Notify the signer without requiring action |
| `in_person` | body | `boolean` | no | Use in-person signing for this signer |
| `signers[].password` | body | `string` | no | Password the signer must enter before signing |
| `verify_phone_number` | body | `string` | no | Phone number required for signer verification Maximum length: 255. |
| `verify_bank_account` | body | `string` | no | Bank account required for signer verification Maximum length: 255. |
| `redirect_url` | body | `string` | no | Signer-specific redirect URL after signing Maximum length: 2100. |
| `redirect_url_declined` | body | `string` | no | Signer-specific redirect URL after declining Maximum length: 2100. |
| `after_document` | body | `string` | no | Document URL that should be signed before this signer |
| `use_stamp_for_approve_only` | body | `boolean` | no | Place an approval stamp when a signer approves the document |
| `redirect_url` | body | `string` | no | Redirect users here after signing Maximum length: 2100. |
| `redirect_url_declined` | body | `string` | no | Redirect users here after declining Maximum length: 2100. |
| `is_being_prepared` | body | `boolean` | no | Have the sender prepare the document before sending |
| `required_attachments[]` | body | `array<object>` | no | Attachments that signers are required to upload |
| `disable_attachments` | body | `boolean` | no | Disable uploading or adding attachments |
| `disable_text_signatures` | body | `boolean` | no | Disable typed text signatures |
| `disable_text` | body | `boolean` | no | Disable adding text |
| `disable_date` | body | `boolean` | no | Disable adding dates |
| `disable_upload_signatures` | body | `boolean` | no | Disable uploaded image signatures |
| `force_signature_color` | body | `string` | no | Force a specific signature color Maximum length: 100. |
| `disable_blockchain_proof` | body | `boolean` | no | Disable storing timestamp proof hashes in blockchain integrations |
| `text_message_verification_locked` | body | `boolean` | no | Require text message verification before the signer can view the document |
| `integration` | body | `list<string>` | no | Integration identifier for the SignRequest record Accepted values: `formdesk`, `mfiles`, `microsoft-flow`, `salesforce`, `zapier`. |
| `integration_data` | body | `object` | no | Integration-specific payload for the SignRequest |
