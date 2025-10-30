# netsurf-disclosure

This repository contains technical details and proofs of concept for three vulnerabilities in NetSurf 3.11.

* [**CVE-2024-51317**](CVE-2024-51317): Use-after-free in `dom_node_normalize`, confirmed to allow remote code execution by malicious web pages when JavaScript is enabled. Full exploit code will be published at a later date.
* [**CVE-2025-29699**](CVE-2025-29699): Use-after-free in `dom_node_set_text_content`, potentially allowing remote code execution by malicious web pages when JavaScript is enabled (impact not yet confirmed).
* [**CVE-2025-45663**](CVE-2025-45663): Incomplete initialization of the `dom_event` structure by `_dom_event_initialise`, providing a partial information leak primitive for other exploits when JavaScript is enabled.

All vulnerabilities have been patched in the affected library, [libdom](https://www.netsurf-browser.org/projects/libdom/). However, as of October 28, 2025, the developers have not yet published a full release of NetSurf that includes these fixes. To mitigate the issues, users should build NetSurf from the project's Git repositories, rather than from the source archives on the main website. Instructions for doing so can be found here: https://ci.netsurf-browser.org/jenkins/job/docs-netsurf/doxygen/md_docs_quick-start.html
