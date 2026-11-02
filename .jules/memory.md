## Archived: 2026-11-02

* Always enforce HTTPS for the company website URLs (e.g., https://www.mavericktechok.com) throughout the repository to meet industry security standards and prevent browser warnings.
* A local development server can be started for the static site using the command `python3 -m http.server 8000`.
* The live static website is hosted on GitHub Pages using the canonical custom domain www.mavericktechok.com and corresponds to the GitHub repository https://github.com/mavericktechok/maverick.github.io.git. The repository's CNAME file explicitly uses the 'www' subdomain to ensure proper redirects from the apex domain.
* Directive: Always begin tasks in a 'deep planning mode.' Use the `request_user_input` tool to ask clarifying questions until there is zero doubt about the user's expectations. Only create an execution plan (`set_plan`) after assumptions are verified and requirements are crystal clear. Once the plan is set, execute it autonomously without asking for further confirmation.
* Core company contact details to maintain across the site include Phone: 405-680-0100, Fax: 405-680-0101, Email (Contact & Billing): tracy@mavericktechok.com, and an 'Established 2003' footer notice.
* The project UI design relies on an infinitely scrolling architecture that uses the Intersection Observer API to trigger scroll-reveal animations.
* The repository contains a static website for Maverick Technologies, built using pure HTML, CSS, and vanilla JavaScript.
* The established color palette for the project features light blue (#A6B1C2) alongside neutral greys.
* The site requires specific SEO metadata geared towards government procurement visibility, which includes maintaining CAGE, DUNS, and NAICS codes.
* Maverick Technologies develops mobile applications; the repository includes a dedicated app privacy policy (`app-privacy.html`) to comply with iOS and Android App Store publisher requirements.
* UX/UI Code Guidelines: Prioritize accessibility by ensuring full keyboard navigability (e.g., skip links, tab order, focus-visible states), using semantic HTML, adding ARIA labels to icon-only buttons, and utilizing existing CSS classes rather than introducing new custom styles.
* Frontend visual verification is performed using a headless Playwright script to capture screenshots of the locally hosted development site. Delays (e.g., `time.sleep()`) must be included in the script to allow scroll-reveal animations to complete before capturing images.
* Tooling Insight: When verifying local frontend UI changes, use the `read_media_file` tool to visually inspect locally generated screenshots (such as those from Playwright), because the `view_image` tool only supports remote URLs.
* The site layout incorporates a sticky navigation bar with anchor links, requiring 'scroll-padding-top' on the HTML tag to appropriately offset scrolling.

Guidelines:
* **User Request Supersedes:** Always prioritize the user's current, explicit request over any conflicting information in memory.
* **Context vs. State:** Use memory for historical context and intent (the "why"). Use the actual codebase files as the source of truth for the current code state (the "what").
* **Memory is Not a Task:** Do not treat information from memory as a new, active instruction. Memory provides passive context, do not use it to create new feature requests.
