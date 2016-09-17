#### Tradera Selling Experience

Tradera, a Swedish online marketplace for auctions and retail, needed a new selling experience. I drove a complete redesign of the item listing flow, as well as several major features that drove customer satisfaction and sales growth.

#### The design strategy

**Make it feel fresh.** I made the selling experience match the overall feeling of the rest of Tradera - clean, simple, minimal, and very Scandinavian. 
**Simplify difficult tasks.** A few parts of the selling process had steep learning curves, so we devoted extensive resources to make them error-proof.
**Save customers time.** We know many people base their livelihoods around selling on Tradera, so we added new features to boost productivity.
**Create a robust platform.** The new simpler code base made the experience fast and easy to maintain - letting us safely add important new features.

#### Selling: adding two steps made it faster

Although it may seem paradoxical, by changing the selling process from one long page to three shorter ones, we were able to use those transitions to implement new functionality to save customers - and ourselves - a lot of time and effort. 

By creating explicit ‘check points’ in the flow, we make decisions based on the information gathered so far to automate tasks, and pare down a considerable amount of error handling code, messaging, and edge cases.

#### Step 1-2: Automatic category selection

Let’s say the customer is selling a 64gb iPhone 5s. In the old Tradera, customers had to drill down through a tree-like structure of literally hundreds of possible choices to put it in the place where it belongs - Mobile & Telecom > Phones > iPhone. 

Now, after we gathered their item description, we use the transition from Step 1 to Step 2 to search against our product categories and automatically present the most likely choice. 

**Result**: This feature fixed the number one customer service issue in the sales flow, and reduced the error rate of people choosing the wrong category by over 90%. 

#### Step 2-3: Automatic payment and shipping

Let’s say the customer trying to sell that iPhone is brand new to Tradera, and has no reputation or history. Before, buyers wouldn't trust them and their phone wouldn't sell - disappointing everyone.

Now, we use the transition from Step 2 to Step 3 to constrain those sellers to offer Buyer Protection. That means payment is secure (via Klarna) and shipment is insured and traced (via DB Schenker). 

**Result**: New sellers are more successful, buyers can purchase with confidence, and we were able to offer this feature while simultaneously stripping out redundant code.

#### Leaner, lighter, quicker code

The previous experience used extensive jQuery animation to make the page expand, collapse, and otherwise move around dynamically. That made it irritating, buggy, and slow.

**Result.** The new experience is attractive, clean, and usable. Due to the removal of all the extraneous animation and code, it's noticeably faster on mobile. It even *shipped* faster - the new site went from concept to launch in less than 1/3 of the time of the previous version.

#### New feature: templates

Customer interviews revealed a pressing problem; time wasted repeatedly creating the same ad with only slight variations. So, we piloted a lightweight 'Templates' feature to prove the hypothesis. It was such a success, sellers quickly moved their entire workflow to templates, then flooded us with suggestions on how to make them even better. We built it into a full feature, then released it to everyone.

**Result**: Right now, templates are now being used to list over *40% of all ads* on Tradera. The feature saves some of our sellers over an hour per day.

#### New feature: persistent draft

One of our engineers had been working on a hackathon project to automatically save the current state of an in-progress ad to the customer's account. So, for example, if they close their browser window, then come back to Tradera days or weeks later, the ad will be there, exactly where they left off. 

I mapped out the use cases and discovered that we needed some additional choices to handle some unintended consequences. (For example, it was too hard to delete an ad and start over fresh, so we added it.) 

**Result**: A quick pilot proved that this was such a delighter we quickly released the full feature. It remains a key differentiator of Tradera's selling experience.

#### New feature: charity support

Every year, Tradera supports a charity event called Musikhjälpen. Sellers can donate products for sale, and the proceeds get donated to the campaign each year. Items can only be offered for sale in certain categories, and require very specific payment and shipping options, which has been confusing for customers in the past.

The step-by-step nature of the new experience meant we could greatly simplify the process for sellers - selecting the right category, shipment and payment options with a single click - and we shipped this new capability in two weeks.

#### Overall results

**Massively improved cohort analysis results.** We measure the likelihood of a given customer to sell an item on successive months. The old interface actually dissuaded use - people were 15% less likely to list the next month after using it. The new one now makes people 50% more likely to list something again the next month.

**Significantly improved usability.** By removing obstacles, stripping out unnecessary edge cases, we improved the experience in ever way. We have greatly reduced customer service calls, increased net promoter scores, speed up the listing process, and made our customers happier.

**Lean, maintainable code.** The redesign has 80% less Javascript code and fewer jQuery libraries, which makes the whole experience faster and easier to work with.

**New extensibility.** The new experience is open and 'light' and flexible, which allowed us to pilot and launch three new core capabilities within 6 months.

**Robust platform.** The new experience allows us to quickly implement new payment and shipping options to support important marketing events, as well as respond to events outside our control.



———

V1 scraps

(When creating an ad, a customer has to provide some pictures, create a title, write a description, choose whether to list it as an auction or ‘buy now’, etcetera. (If you’ve ever used eBay you know what this is.) The previous code base - the one that had lasted for ten years - did this all on one long page, with minimal help or flair. It was a typical web form.

The redesign I walked into tried to modernize it with a very rich, dynamic, javascript/css driven interface. Elements expanded when first interacted with, then contracted to show a short ‘preview’. Whole sections of the interface would appear and disappear at a click. The problem was, all this stuff moving around and hiding was incredibly confusing. 

Even worse, it was completely out of step with the way the rest of the site behaved. Instead of being different where it needed to be, it was different for it’s own sake, and far more complex and fidgety than necessary. Even the visual design was off; the new Tradera was clean, open, modern and spare, while the new selling screen was complicated, cramped, and overdone.

The last part of the challenge was making the experience feel new and modern enough to be accessible to young, new customers, while not alienating the loyal customers that had over a decade of experience with the old way of doing things. I was scrupulous about finding ways to refresh and modernize the way the experience felt, without making unnecessary changes to the fundamentals.)
