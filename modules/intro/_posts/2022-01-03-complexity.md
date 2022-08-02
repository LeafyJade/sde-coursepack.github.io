---
Title: Software Complexity
---

Software failures are easy to occur because software is so complex.

Look at Google.com: 

![alt]({{site.baseurl}}/img/google.png)

Seems simple enough! What's that, like 20-30 lines of code, right? In most browsers, you can right click on the page and go to View Source. Here's what you'll see:

![alt]({{site.baseurl}}/img/googleSource.png)

This page has a massive source code base! Each of these lines you are seeing are large functions, with hundreds of lines, variables, etc. And yet, you've almost certainly never dealt with any of this code before. That's because, as a user, you are on the customer side. If you need to ever even *see* at source code of software you are using at a consumer level, chances are something has gone very wrong.

# Why do we write software?

We write software to *solve problems.* That problem might be "When is my next meeting?", or "I need to book a flight", or "who won the football game last night", or even "I'm bored, let me play a game to stave off this boredom." Many of the problems we solve had solutions before software, but software can make it easier, more efficient, and more accurate. 

And yet, even simple sounding problems can have tons of hidden complexities.

# George Washington's Birthday

Let's write a program to tell us how many days old George Washington is. How hard can this be?

Well, since we're here, let's ask Google.

![alt]({{site.baseurl}}/img/washingtonWUT.png)

Wait, what!?!? So which is it? February 22, 1732, or February 11, 1731? To add to the confusion, the Washington family Bible notes that George Washington was born "11th Day of February, 1731/2". And even if we could pick a date, as we go back through the calendar of England, which was the calendar used in the colonies, we see this:

![alt]({{site.baseurl}}/img/September1752.png)

Where did those days go? Well, as some of you may have guessed, this has to do with religion. In 1582, the then Pope Gregory XIII introduced the Gregorian Calendar. However, many Protestant (non-Catholic Christian) countries continued to use the Julian calendar that was already in place for centuries. A relevant detail is that the "first day of the year" used to be considered "the first day of Spring." And as such, March 25 was "New Year's Day" in England during and after the Middle Ages. So February 11, 1731 (Julian) *is the same day* as February 22, 1732. However, England (and by extension the Colonies) adopted the Gregorian calendar in 1752. But all of this means your program could have produced incorrect output if you didn't know and account for this history ahead of time!

Time presents all sorts of challenges, as shown in the Numberphile video below.

<iframe width="560" height="315" src="https://www.youtube.com/embed/-5wpm-gesOY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# The Software Crisis

Many are familiar with [Moore's Law](https://en.wikipedia.org/wiki/Moore%27s_law), which describes the increase in complexity of computer hardware over time. And while there can be dispute over if or when Moore's Law died or will die, what cannot be disputed is the absolute meteoric growth in computing power in the last nearly 80 years since the construction of [ENIAC](https://en.wikipedia.org/wiki/ENIAC). A common saying is that your phone has more processing power than the Apollo program, though don't confuse that with being more capable for the task.

However, while hardware grew exponentially faster and faster for decades, the software that used the hardware...didn't. By the 1960s, software was already seen as behind. While the machines got more and more powerful year after year, programming skills, techniques, and abilities weren't improving at the same rate. The bottleneck for major computing undertakens became more about the programming than about the computing resources. This became known as the "software crisis".

Unfortunately, this remains an unsolved problem. In 1986, Fred Brooks wrote, in his famous essay "No Silver Bullet":

*"There is still no single development, in either technology or management technique, which by itself promises even one order-of-magnitude improvement with a decade in productivity, in reliability, in simplicity."

What has happened since? Have we seen any improvement? Yes! But, Fred Brooks is still right. Software development methodologies have improved efficiency. Libraries and APIs have improved code reusability. Things have gotten better, but we still have significant difficulty. We still haven't seen a velocity of improvement even *close* to hardware resources.

<img src="https://csdl-images.ieeecomputer.org/mags/so/2008/01/figures/mso2008010091x1.gif" alt="Cover of IEEE's Computer Magzine from April 1987, which featured 'No Silver Bullet'.">

# No Silver Bullet

Take a moment and read the first 4 pages or so of [No Silver Bullet](http://worrydream.com/refs/Brooks-NoSilverBullet.pdf). You will, however, be expected to read the whole article for class. Proceed after you have read.

## Essential and Accidental Difficulties

One of the key takeaways from No Silver Bullet is that 
software difficulty is made up of difficulties that are 
**essential** and **accidental.**

**Essential** difficulties are that are intrisic to developing software. These difficulties cannot be seperated from the software development process.

**Accidental** difficulties emerge because of circumstance. For example, in the 1960s, most programs were written on pencil and paper, and transcribed into punch cards. This process was slow, and great care had to be taken to ensure cards were punched correctly and ordered correctly. These difficulties can be address by improved technology (like keyboards, IDEs, GUIs, etc.). 

Imagine if you had a stripped screw that you were trying to unscrew. The fact that it's difficult to unscrew isn't *essential*, as if the screw weren't stripped, it would be very easy. However, if I asked you to "build a bookshelf", then that is *essentially* more complicated than unscrewing a screw, even if you removed all *accidently complexity* and shop at IKEA for "Billy" the bookcase.

<img src="https://www.sheknows.com/wp-content/uploads/2018/08/ikea9_svxdy8.jpeg" alt="Ikea's Bookcase has seen better days">

The crux of Brooks's argument is that *there are essential difficulties* that will never completely go away. Developing software will always be hard, even as our technological and methodological improvements gives us more power to thwart the *accidental complexities*. That is, while technology can help us be better and more efficient at writing code, it doesn't help us solve problems related to *specification*, *design*, etc.

And this idea has held up. "No Silver Bullet" is considered among the most, if you'll excuse the word, *essential* readings for software engineers. In February 2021, IEEE's Computer Magazine published ["There Is Still No Silver Bullet"](https://www.computer.org/csdl/magazine/co/2021/02/09353507/1r8krp0NNK0), a reflection nearly 35 years after No Silver Bullet was published. To quote the author, David Alan Grier, *"Yet, almost 35 years after he wrote this contribution to knowledge, Brooks’s observation remains true. Software engineering is a complex and demanding field that poses a host of problems to the practitioner, and there is no single solution, that is, no silver bullet, that will provide a simple way to reduce the work required to create a software product."

That is, programming is hard because the problems we are solving are themselves hard, full of hidden complexity. And if you still aren't convinced, I have only one question:

How many seconds old is George Washington (be sure to include time zones, [leap seconds](https://en.wikipedia.org/wiki/Leap_second)) and Daylight Savings Time where appropriate. Also, be aware that any consider for Daylight Savings in your solution has to work differently for people in Arizona, and [might have to change in 2023](https://www.congress.gov/bill/117th-congress/senate-bill/623/text).