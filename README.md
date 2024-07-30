# Mobile Abuse Reporting Schema 

## Table of Contents

- [Mobile Abuse Reporting Schema](#mobile-abuse-reporting-schema)
  - [Overview](#overview)
  - [Schema Details](#schema-details)
  - [Schema Definition](#schema-definition)
  - [Examples](#examples)
  - [Contributing](#contributing)

## Overview

The Mobile Abuse Reporting Schema is a JSONSchema specification providing a standardized structured format for end user messaging clients to provide feedback about abusive or misclassified mobile messages.

## Schema Details

- Title: Mobile Abuse Reporting Schema
- Description: Specification for reporting mobile messaging abuse and misclassified abuse.
- Schema Format: JSONSchema Draft 2020-12
- Copyright: © 2024 by Proofpoint Inc.
- License: [LICENSE](./LICENSE)

## Schema Definition

- Schema: [schema.json](./schema.json)

## Examples

```json
  {
    "v": "1",
    "u": "OrganizationA/Messages/2.3-alpha",
    "s": "+1234567890",
    "d": "spam",
    "m": {
      "p": "sms",
      "t": "2024-03-12T15:45:22Z",
      "c": "Elevate your look at TrendSetter.com! Unleash your unique style with our exclusive collection. Shop now, before it's gone!"
    }
  }
```

```json
  {
    "v": "1",
    "u": "OrganizationB/Messenger/2.2.3",
    "s": "+1234567890",
    "r": "+1555123456",
    "d": "legit",
    "m": {
      "p": "mms",
      "t": "2024-03-12T15:45:22Z",
      "c": "Content-Type: multipart/mixed; boundary=\"boundary-example\"\r\n\r\n--boundary-example\r\nContent-Type: text/plain; charset=\"UTF-8\"\r\n\r\nThis is the text part of the message.\r\n\r\n--boundary-example\r\nContent-Type: image/jpeg\r\nContent-Transfer-Encoding: base64\r\n\r\n<base64_encoded_image_data>\r\n\r\n--boundary-example--"
    }
  }
```

```json
  {
    "v": "1",
    "i": "20275d91-690f-4908-a191-f1a16d0a770b",
    "u": "OrganizationC/Messenger/v2-alpha",
    "s": "+447700900123",
    "r": "ec4333c7b178abddf8885c1c357bfe952c9c886a53d4ad93f936fb42c0f7588e",
    "m": {
      "p": "rcs",
      "t": "2024-03-12T15:45:22Z",
      "c": "Content-Type: text/plain; charset=\"UTF-8\"\r\n\r\nBuy v1agra here: http://example.net"
    }
  }
```

```json 
  {
    "v": "1",
    "u": "OrganizationD/Messages/3.6.0GA",
    "s": "+1234567890",
    "m": {
      "p": "sms",
      "t": "2024-03-12T15:45:22Z",
      "c": "Contact 888-555-000 immediately to claim your prize!"
    }
  }
```

## Contributing

We welcome contributions to improve this project! If you find any issues, errors, or have suggestions for enhancements, please follow the guidelines below to help us address them effectively.

### Reporting Errata

1. Search Existing Issues: Before reporting a new erratum, please check the existing issues to see if it has already been reported. This helps prevent duplicates and allows us to track issues more efficiently.

2. Open a New Issue:
    - Go to the Issues tab.
    - Click on "New issue".
    - Use the template provided or include the following information:
      - Title: Brief summary of the issue.
      - Description: Detailed description of the erratum, including steps to reproduce it if applicable.
      - Expected Behavior: What you expected to happen.
      - Actual Behavior: What actually happened.
      - Additional Context: Any other relevant information, such as screenshots, logs, or links.
3. Labeling: Add the label errata to your issue to help us categorize and prioritize it.

### Suggesting Improvements

1. Search Existing Issues: Check the existing issues for similar suggestions to avoid duplicates.
2. Open a New Issue:
    - Go to the Issues tab.
    - Click on "New issue".
    - Use the template provided or include the following information:
      - Title: Brief summary of the suggestion.
      - Description: Detailed explanation of your suggested improvement, including why it would be beneficial.
      - Additional Context: Any other relevant information, such as mockups, references, or links.
3. Labeling: Add the label enhancement to your issue to help us categorize and prioritize it.

### Contribution Guidelines

- Be Clear and Concise: Provide as much detail as necessary to understand and reproduce the issue or suggestion, but keep it concise and to the point.

- Respectful Communication: Use respectful and constructive language when reporting issues or suggesting improvements.

- Stay Involved: If we need more information or have questions, please be responsive and provide the necessary details.

Thank you for contributing to this project! Your feedback and suggestions help us improve and deliver a better experience for everyone.
