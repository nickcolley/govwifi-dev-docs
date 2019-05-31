# Govwifi developer documentation

This is the technical documentation for the [Govwifi](https://www.wifi.service.gov.uk/) team in the [Government Digital Service (GDS)](https://gds.blog.gov.uk/). For other projects built by GDS, see the [Service Toolkit](https://www.gov.uk/service-toolkit).

## Applications overview

Our public-facing websites are:

- A [product page](https://github.com/alphagov/govwifi-product-page) explaining the benefits of GovWifi
- An [admin platform](https://github.com/alphagov/govwifi-admin) for organiations to self-serve changes to their GovWifi installation
- [Technical documentation](https://github.com/alphagov/govwifi-tech-docs), explaining GovWifi in more detail
- A [redirection service](https://github.com/alphagov/govwifi-redirect) to handle "www" requests to these sites

Our services include:
- [Frontend servers](https://github.com/alphagov/govwifi-frontend), instances of freeRADIUS that act as authentication servers

- An [authentication API](https://github.com/alphagov/govwifi-authentication-api), which the frontend calls to help authenticate GovWifi requests
- A [logging API](https://github.com/alphagov/govwifi-logging-api), which the frontend calls to record each GovWifi request
- A [user signup API](https://github.com/alphagov/govwifi-user-signup-api), which handles incoming sign-up texts and e-mails (with a little help from AWS)

We manage our infrastructure via:

- Terraform, see [govwifi-terraform](https://github.com/alphagov/govwifi-terraform)
- The [safe restarter](https://github.com/alphagov/govwifi-safe-restarter), which uses a [CanaryRelease](https://martinfowler.com/bliki/CanaryRelease.html) strategy to increase the stability of the frontends

Other repositories:

- [Acceptance tests](https://github.com/alphagov/govwifi-acceptance-tests), which pulls together GovWifi end-to-end, from the various repositories, and runs tests against it.