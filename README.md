# BitLeaks by Reconquest
## Bitbucket Add-On

### Installtion

Add-on can be installed from [Atlassian Marketplace][1].

### What this add-on provides?

BitLeaks add-on enhaces security of your organization by preventing secret
information leaks into source code repositories.

### Detected secrets

BitLeaks add-on detects attempts to push following cryptographic keys & secret
tokens:

* Private Keys:
    * RSA
    * SSH
    * PKCS8
    * PGP
    * EC
* AWS Credentials:
    * AWS Client IDs
    * AWS Secret Keys
    * AWS MWS Keys
* Facebook Credentials:
    * Facebook Client IDs
    * Facebook Secret Keys
    * Facebook Access Tokens
* Twitter Credentials:
    * Twitter Client IDs
    * Twitter Secret Keys
* Github Secret Keys
* LinkdIn Client IDs
* Slack Credentials:
    * Slack Auth Tokens
    * Slack Webhooks
* Generic API Keys (starting with `api_key` or `apikey`)
* Generic Secret Strings (starting with `secret`)
* Google Credentials:
    * Google API Keys
    * Google Cloud Platform API Keys
    * Google OAuth Tokens
* Heroku API Keys
* MailChimp API Keys
* MailGun API Keys
* Passwords in URL
* PayPal Access Tokens
* Pacatic API Keys
* Stripe API Keys
* Square Credentials:
    * Square Acess Tokens
    * Square Oauth Secrets
* Twilio API Keys

## Usage

BitLeaks does not provide any configuration options right now.

In order to start preventing secrets leaks into repository just enable BitLeaks
Add-On Hook after installation.

It can be done by navigating into `Repository Settings` → `Hooks` in Bitbucket
interface and enabling it from there:

<img src="docs-screens-1.png"/>

## Testing

Try to push file with following contents into repository:

```
-----BEGIN OPENSSH PRIVATE KEY-----
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
-----END OPENSSH PRIVATE KEY-----
```

Push will be rejected.

[1]: https://marketplace.atlassian.com/apps/1221119/bitleaks-secrets-leak-security
