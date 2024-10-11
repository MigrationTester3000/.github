# .github


test readme contents

Steps to Set Up the Webhook
- Go to your GitHub organization settings.
- Navigate to "Webhooks".
- Click "Add webhook".
- Set the "Payload URL" to https://api.github.com/repos/<org-name>/.github/dispatches.
- Set the "Content type" to application/json.
- Add a secret if desired.
- In the "Which events would you like to trigger this webhook?" section, select "Let me select individual events" and check "Repositories".
- Save the webhook.
- Example Payload for the Webhook

```
{
  "event_type": "repository_created",
  "client_payload": {
    "repository": {
      "name": "new-repo-name"
    }
  }
}
```

