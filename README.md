# Automated repro for issue 8639

## Versions tested

- 14.7.0 - ci token

  - OK

- 13.21.0

```
Error: HTTP Error: 401, Request had invalid authentication credentials. Expected OAuth 2 access token, login cookie or other valid authentication credential. See https://developers.google.com/identity/sign-in/web/devconsole-project.
[2025-06-18T00:57:57.664Z] Error Context: ***
  "body": ***
    "error": ***
      "code": 401,
      "message": "Request had invalid authentication credentials. Expected OAuth 2 access token, login cookie or other valid authentication credential. See https://developers.google.com/identity/sign-in/web/devconsole-project.",
      "errors": [
        ***
          "message": "Invalid Credentials",
          "domain": "global",
          "reason": "authError",
          "location": "Authorization",
          "locationType": "header"
        ***
      ],
      "status": "UNAUTHENTICATED",
      "details": [
        ***
          "@type": "type.googleapis.com/google.rpc.ErrorInfo",
          "reason": "ACCESS_TOKEN_EXPIRED",
          "domain": "googleapis.com",
          "metadata": ***
            "method": "google.cloud.identitytoolkit.v1.AccountManagementService.DownloadAccount",
            "service": "identitytoolkit.googleapis.com"
          ***
        ***
      ]
    ***
  ***,
  "response": ***
    "statusCode": 401
  ***
***
```

- 13.22.0

```
[2025-06-18T10:08:14.430Z] Running auto auth
[2025-06-18T10:08:14.431Z] TypeError: Cannot read properties of undefined (reading 'access_token')
    at getAccessToken (/home/runner/work/issues-8639-auto/issues-8639-auto/node_modules/firebase-tools/lib/apiv2.js:43:17)
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
    at async RetryOperation._fn (/home/runner/work/issues-8639-auto/issues-8639-auto/node_modules/firebase-tools/lib/apiv2.js:303:40)
```

- 13.0.0

```
Error: HTTP Error: 401, Request had invalid authentication credentials. Expected OAuth 2 access token, login cookie or other valid authentication credential. See https://developers.google.com/identity/sign-in/web/devconsole-project.
[2025-06-18T15:34:14.286Z] Error Context: ***
  "body": ***
    "error": ***
      "code": 401,
      "message": "Request had invalid authentication credentials. Expected OAuth 2 access token, login cookie or other valid authentication credential. See https://developers.google.com/identity/sign-in/web/devconsole-project.",
      "errors": [
        ***
          "message": "Invalid Credentials",
          "domain": "global",
          "reason": "authError",
          "location": "Authorization",
          "locationType": "header"
        ***
      ],
      "status": "UNAUTHENTICATED",
      "details": [
        ***
          "@type": "type.googleapis.com/google.rpc.ErrorInfo",
          "reason": "ACCESS_TOKEN_EXPIRED",
          "domain": "googleapis.com",
          "metadata": ***
            "method": "google.cloud.identitytoolkit.v1.AccountManagementService.DownloadAccount",
            "service": "identitytoolkit.googleapis.com"
          ***
        ***
      ]
    ***
  ***,
  "response": ***
    "statusCode": 401
  ***
***
```
