#### eBay Global Grid System

In 2011, I designed the global layout grid to be used across all eBay web properties. This was the first step in a multi-year redesign initiative. This case study covers the challenges, research, and design thinking behind the system.


#### Creating 'just enough' of a grid

A grid system means content is laid out within a uniform number of rows and columns across the whole site. The challenge with eBay is it's incredibly diversity. It site contains everything from auctions and e-commerce to IAB advertising banners, highly customized vertical marketplaces and even blogs. 

Any system that tried to solve it all would quickly become unwieldy. So, I focused on solving the common high-level structuring and left fine details to each team’s discretion. This was also a transitional tool - a full site redesign wasn't on the table for several years, and we wanted to start building rigor around grids and layout now.

#### Constraints and challenges

**Adoption**. Another challenge is adoption. eBay has a lot of engineering teams spread across a huge campus, and - to be blunt - we didn’t have the authority to force everyone to adopt it. The grid couldn't just make sense in some ideal long term, it had to solve immediate problems for every team.

**Implementation**. The grid also had to be simple to implement too. I’ve seen my fair share of projects that seemed *perfect* to the original team, but were complex or ambiguous enough that they get stonewalled and then quietly dropped. We needed to create something that would be easy to communicate, learn, and adopt. 

[[ The biggest challenges of introducing any global design guidelines are always organizational. ]]

**Left navigation.** The filtering and search tools for eBay reside on the left hand navigation bar, and the code behind them is complex. Touching those beyond some visual restyling was out of the question, so the left navigation needed to be a minimum of 203 pixels wide. 

**Advertising**. We were also incorporating more and more advertising in our shopping experience. So, I took inspiration from Khoi Vinh. When he redesigned the web site for the New York Times, he based the grid system itself around IAB standard ad sizes. I did the same.

#### Screen resolution research

eBay has robust native app strategy for mobile devices, so my focus was on desktop. Trend analysis by companies like Gartner gave us numbers but not design guidelines, so I created the infographic above to visualize exactly how many people would be ‘covered’ by a site optimized for a given screen resolution.

- 70% of our customers use 16:9 wide screen devices. 
- Oddball screen sizes generally differed mostly by height.
- When oddball screens differed by width, it was by fewer than 100 pixels.
- Once I clustered screen sizes together, the vast majority fit into three groups with a fairly regular distribution.

#### Matching screen resolutions to devices

I wanted to see if I could identify future trends in eBay. I then took each screen resolution and compiled lists of the devices that offered them. My conclusions:

- 16:9 Wide screens are on everything now, and should become our default design assumption.
- Of the 30% of customers with standard 4:3 screens, half were iPads, which skew strongly toward our native apps.
- After 1280px wide resolution, which could be seen by 84% of our customers, screen size adoption dropped off a cliff.
- The next wider resolution, 1366px, could be seen by half our customers.
- 1680px or wider could be seen by less than a third. 

#### The final grid design

The final thing that clicked was as I was shopping the problem around to various engineers, one of them griped about odd pixel dimensions. I forget the exact numbers, but he said: 

"I never remember the column widths because they always break down into some oddball number like four at 157 pixels and one that's one pixel off. So I end up winging it."

It then hit me: what’s a nice, round number that is big enough to fit a 203 pixel wide nav bar? 210 pixels.

You know what adds up to 210 pixels? Two 100-pixel columns and a 10-pixel gutter.

You know what makes a numbers-driven system easy to remember and use? Being divisible by ten.

Bingo. We went metric.

#### Results

**Testing**. I beta tested the grid in my own work for a while and found that it worked perfectly. Our layout-heavy screens were almost designed with an asymmetrical layout, and fit into the 7-column content area with minor adjustment.

**Future proofing**. I fleshed out the grid to optimize the experience for larger resolutions. I documented two strategies - making the column width a 100px wide minimum stretching to fill larger screens, or adding two columns dynamically at larger breakpoints and showing/hiding additional widgets, features, and content.

**Launch**. We adopted the grid for all work going forward, distributed the documentation company-wide, and began evangelizing it to other design and engineering teams.

**Adoption**. This grid system was adopted by teams across the retail shopping experience, and continued to be used for years after I left the company. It did it's job as a transitional step to a responsive layout, and stayed in use until the 2015 redesign.