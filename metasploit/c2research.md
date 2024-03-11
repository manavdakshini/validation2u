# C2 Research

- In this activity, you will continue to play the role of a pentester conducting an engagement on MegaCorpOne.
- You are tasked with researching various C2 frameworks by using the [C2 Matrix website](https://www.thec2matrix.com/matrix) and suggesting the best C2 framework for your current assessment on MegaCorpOne.
- You will then answer several questions about the frameworks you select.

### Activity Instructions

Using the [C2 Matrix site](https://www.thec2matrix.com/matrix) and Google, find two C2 frameworks that fit the requirements described below.

**Requirements**

Throughout your initial scans on MegaCorpOne's domain, you've discovered several facts:
- Their network includes mostly Windows machines, with some Linux machines scattered throughout.
- Their firewall rules only allow ports 80, 443 TCP and port 53 UDP outbound

The service contract includes a few additional requirements:
- The C2 framework must support logging.
- The framework must have a full version released&mdash;i.e., the version must be 1.0 or higher. No "beta" or "PoC" versions allowed.
- You will bring on coworkers to help with this assessment, so the framework needs to support multiple users. 

**Note**: It's okay if your primary C2 framework does not support all operating systems, as long as the secondary or tertiary framework supports the systems that the primary framework does not.