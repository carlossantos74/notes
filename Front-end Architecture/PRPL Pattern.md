The PRPL pattern focuses on four main performance considerations

#### P - Push critical resources for the initial route
Pushing critical resources efficiently minimizes the number of round trips to the server and reduces the loading time.

Which means: For the very first page or route a user visits, you want to get the minimal set of code and assets required to display meaningful content as quickly as possible.

#### R - Render the initial route as soon as possible
Rendering the initial route as soon as possible improves the user experience.

Which means: Once the critical resources have arrived, render the initial view immediately. The user should see something on the screen as quickly as possible, ideally within a few hundred milliseconds.

#### P - Pre-cache remaining routes
Pre-caching assets in the background for frequently visited routes minimizes the number of requests to the server and enables a better offline experience.

Which means: After the initial route is rendered, proactively store the assets and data needed for other important pages in the cache (often using a service worker) so that future navigations are extremely fast. This includes JavaScript bundles for other parts of the site, images, and possibly JSON data.
##### L - Lazy-load other routes on demand
Lazy-loading routes or assets that aren’t requested as frequently.

For pages or features that are not critical to the main user flows, don’t load them upfront. Instead, fetch these resources only when the user needs them. This approach ensures you don’t bloat the initial load time with unnecessary assets.



--- 
### References: 
- https://www.patterns.dev/vanilla/prpl/
- https://github.com/carlossantos74/PRPL-app