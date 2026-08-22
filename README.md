# Nuvei (nuvei)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Nuvei is a global payment technology company headquartered in Montreal, Canada, providing a single platform for online card acquiring, alternative payment methods (700+ APMs), payouts, currency management across 150+ currencies, risk and fraud, and payment orchestration. Nuvei serves merchants in 200+ markets with local acquiring in 52 markets across eCommerce, iGaming, sports betting, travel, retail, B2B, and financial services. Originally listed on Nasdaq and TSX as NVEI, Nuvei was taken private by Advent International in 2024.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/nuvei/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/nuvei/refs/heads/main/apis.yml)

## Tags

- Payments
- Payment Processing
- Payment Gateway
- Acquiring
- Payouts
- Alternative Payment Methods
- Fraud
- Risk
- Currency Conversion
- iGaming
- eCommerce
- FinTech

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Nuvei Payments API

Server-to-server REST API for processing card and APM transactions through Nuvei. Includes openOrder for session setup, payment for end-to-end transactions, settleTransaction for capturing pre-authorized amounts, refundTransaction for refunds, voidTransaction for cancellations, and getPaymentStatus for transaction state. Auth uses SHA-256 checksum over merchantId, merchantSiteId, clientRequestId, amount, currency, timeStamp, and merchantSecretKey.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Payments
- Authorization
- Settlement
- Refund
- Void

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-payments-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-payments-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-payments-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/nuvei-payment-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/nuvei-transaction-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Nuvei Session API

Generates and manages session tokens (getSessionToken) used to authenticate subsequent REST calls and Web SDK operations. Session tokens are scoped to a merchant and order and have a short lifetime.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Sessions
- Tokens
- Authentication

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-session-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-session-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-session-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei Order API

Creates and updates orders prior to payment via openOrder and updateOrder. Supports line items, billing/shipping addresses, currency, device details, and dynamic descriptors. Used as the first step for Web SDK, Simply Connect, and Payment Page integrations.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Orders
- Cart
- Checkout

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-order-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-order-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-order-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei Payouts API

Pushes funds out to consumers and counterparties via card, bank account, and a wide set of local APMs. The payout endpoint supports referenced (relatedTransactionId) and unreferenced (account number / IBAN) payouts and integrates with accountCapture to collect destination details safely.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Payouts
- Withdrawals
- Disbursement

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-payouts-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-payouts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-payouts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei User Payment Options API

Manages stored payment instruments (User Payment Options / UPOs) including card and APM tokenization. Supports addUPOCreditCard, addUPOAPM, editUPOCreditCard, editUPOAPM, deleteUPO, getUserUPOs, and enableUPO/disableUPO.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Tokens
- Vault
- User Payment Options
- Cards

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-user-payment-options-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-user-payment-options-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-user-payment-options-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei Merchant Configuration API

Returns configuration data for a merchant including supported countries (getMerchantCountries) and the active set of payment methods per country (getMerchantPaymentMethods). Used by client checkouts to render dynamic payment selection.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Merchant
- Configuration
- Payment Methods
- Countries

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-merchant-config-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-merchant-config-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-merchant-config-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei 3DS API

3D Secure 2 authentication endpoints. getCard3DDetails returns DS information and challenge requirements for a card; authenticate3d completes the authentication flow returning CAVV and ECI. Designed to satisfy PSD2 SCA requirements for EEA acquiring.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- 3DS
- SCA
- Authentication
- Cards

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-3ds-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-3ds-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-3ds-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei DCC API

Dynamic Currency Conversion. getDccDetails computes the converted amount and markup rate for a card BIN and currency pair so merchants can present a localized currency offer at checkout.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- DCC
- Currency Conversion
- FX

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-dcc-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-dcc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-dcc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei Direct Merchant Notifications (DMN)

Asynchronous webhook notifications sent from Nuvei to a merchant endpoint to communicate the final status of payments, payouts, refunds, voids, settles, and Control Panel events. Payment DMNs include an advanceResponseChecksum signed with the merchantSecretKey using SHA-256 over the ordered parameter values; withdrawal DMNs concatenate name=value pairs with the secret appended.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/webhooks/](https://docs.nuvei.com/documentation/integration/webhooks/)

#### Tags

- Webhooks
- Events
- Notifications
- DMN

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/)
- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/payment-dmns/)
- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/withdrawal-dmns/)
- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/control-panel/)
- [AsyncAPI](asyncapi/nuvei-dmn-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/nuvei-3ds-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-3ds-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-dcc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-dcc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-merchant-config-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-merchant-config-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-order-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-order-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-payments-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-payments-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-payouts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-payouts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-session-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-session-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-user-payment-options-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-user-payment-options-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [SDK](https://github.com/Nuvei/nuvei-server-php)
- [SDK](https://github.com/Nuvei/nuvei-server-java)
- [SDK](https://github.com/Nuvei/nuvei-server-java-2.0)
- [SDK](https://github.com/Nuvei/nuvei-server-nodejs)
- [SDK](https://github.com/Nuvei/nuvei-mobile-sdk-android)
- [SDK](https://github.com/Nuvei/nuvei-mobile-sdk-ios)
- [SDK](https://github.com/Nuvei/nuvei-react-native-mobile-sdk)
- [SDK](https://github.com/Nuvei/nuvei-mobile-cashier-helper-android)
- [SDK](https://github.com/Nuvei/nuvei-mobile-cashier-helper-ios)
- [SDK](https://github.com/Nuvei/nuvei-cashier-helper-react-for-android)
- [SDK](https://github.com/Nuvei/nuvei-mobile-pods)
- [SDK](https://github.com/Nuvei/nuvei-maven-android)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-magento-2)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-woocommerce)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-prestashop)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-opencart-3)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-opencart-4)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-shopware-5)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-shopware-6)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-salesforce-commerce-cloud)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-sap-commerce)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-commerce-tools-backend)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-commerce-tools-frontend)

## Maintainers

**FN:** Kin Lane
**URL:** https://kinlane.com
