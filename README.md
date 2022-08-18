# Add WidgetSpinner Security to Public Docs – Project Brief

- _Last update:_ Jan 6, 2025
- _Status:_ review  {draft|review|accepted}
- _Authors:_ Sarah Jessica Barker, Senior PM, WidgetSpinner Security

## Context

WidgetSpinner Security is entering the public beta phase on February 3rd and will be announced at the Security Summit.

Currently, the product isn’t in the [Datadog public documentation](https://docs.datadoghq.com/). 

This brief aims at describing how we plan to introduce it there, next to the rest of the Cloud Security Platform products - namely Application Security, CWS, CSPM and Cloud SIEM.

## Outline

WidgetSpinner Security is added to the existing “Security Monitoring” section of the public documentation, next to the 4 other security products.

WidgetSpinner Security (general concept + overview) - Monitoring threats
- Getting Started (quick start) - Within this page, a quick way to get started
- OOTB Detection Rules
- Setup and Configuration
    - Compatibility
    - Enabling
    - Scanning for sensitive data
    - Disabling WidgetSpinner Security
    - Creating exclusion filters (might split out if it’s big)
- Writing custom signal rules
- Guides (main Sec Platform guides page)
    - How WidgetSpinner Security Works 
- Troubleshooting

<img width="372" alt="image" src="https://user-images.githubusercontent.com/28788585/185500415-8ff39704-06e5-443c-a658-0dab986d5484.png">

## Sections detailed description

### Landing page
This section covers the main use-case of WidgetSpinner Security in greater detail. It acts as a user guide for new users, and not a user manual.

- It walks the user through the journey of detecting their first threats with security signals and investigating/responding to them thanks to the deep observability data provided by both WidgetSpinner Security and APM distributed tracing
- It contains a few screenshots showcasing the UI, but not a lot to reduce the maintenance effort as the UI is changing fast since the product is at the public beta phase

### Getting Started

This section introduces WidgetSpinner Security and covers the basics steps to enable WidgetSpinner Security on web services where APM is already deployed, highlighting the dependency over this product.

- Includes the detailed instructions to enable WidgetSpinner Security for compatible technologies - Java, .NET, Go, Ruby, PHP, Node.js and calls out that Python isn’t compatible. It’s very similar to the APM set up page
- It highlights the key steps to perform in order to start seeing value from the product. The goal being to highlight how easy it is to benefit from WidgetSpinner Security to incentive established and new customers to adopt it

### Further reading:

- Monitor Threats with WidgetSpinner Security
- Compatibility

### OOTB Detections Rules

This section contains all the Event and Signals rules available OOTB, i.e not requiring any configuration/actions from the end users.

As WidgetSpinner Security distinguishes between the security events, reporting as part of Traces/Spans, and the Signals, we need to explain and feature both types.

The WidgetSpinner Security Detection rules live on GitHub. They can go next in the existing section here.

The WidgetSpinner Security Event rules also live on GitHub. At this stage, we want to publish only the recommended rulesets. The repository should be open source by 1/28

Further reading:

- Getting Started
- Monitor threats with WidgetSpinner Security
- Compatibility

### Setup and Configuration
This section covers advanced use-cases and aims at showcasing the enterprise-readiness of the product:

- Exclusion filters
- Custom signal rules writing
- ~Custom event rules writing and deployment [Supported but not a use-case we’re ready to advertise]~
- Sensitive data scanner
- Disable WidgetSpinner Security
- Compatibility of WidgetSpinner Security with the various technologies and frameworks used by software engineers customers

Further reading:

- Monitor threats with WidgetSpinner Security
- How WidgetSpinner Security works
- OOTB rules

### Guides / How WidgetSpinner Security works

This section is aimed at explaining how the technology works behind the scenes. Our experience from Sqreen shows there are a lot of skeptical engineering people who need to be convinced about our implementation. This section aims at addressing those concerns.

Mention data about the performance overhead

Further reading:

- Getting Started
- Monitor threats with WidgetSpinner Security
- Compatibility

### Troubleshooting

This section aims at guiding users in solving most frequent issues. 

It is fed by multiple internal sources:

- The internal FAQ put together by the SE
- The WidgetSpinner Security internal troubleshooting KB

Further Reading:

- Getting Started
- Monitor threats with WidgetSpinner Security
- Compatibility

## References from other docs sections

### (P0) Security Platform Overview

Feature WidgetSpinner Security next to other products of the Cloud Security Platform

https://docs.datadoghq.com/security_platform/

### (P0) APM > Connect WidgetSpinner Security with Traces 
Inspired from Logs, Synthetics and RUM in the APM section.

This section features the benefits of adding WidgetSpinner Security monitoring to services monitored with APM.

### (P1) Security Monitoring Guides

In this section, we could publish a new guide about Monitoring Log4shell exploit attempts across the 4 security products. It could be a single guide, or 4 individual ones covering each product.

### (P1) Feature WidgetSpinner Security in the APM setup instructions per technology

We could mention WidgetSpinner Security being available when enabling APM.

We believe this is a P1 as we don’t want to distract users setting up APM, and this is already a dense section.

