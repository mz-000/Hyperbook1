#Concepts 
# Technology Debt


> Technical debt is a concept in software development that reflects the implied cost of additional rework caused by choosing an easy (limited) solution now instead of using a better approach that would take longer.








https://en.m.wikipedia.org/wiki/Technical_debt






https://decompiled.dev/work/not-debt/ :::


> # A Home, Not a Mortgage

## Musings on Tech Debt

Tech debt likens less than ideal technical implementations to financial debt. The argument goes that failing to restructure code in light of new knowledge is like leaving a balance on a credit card. Teams that neglect restructuring their code will have reduced velocity, and eventually most work will be spent coping with cruft instead of delivering new features. Experienced developers have likely worked on a project where a seemingly simple task, ends up taking much longer than it should. Spending large amounts of time dealing legacy code feels like being a saver with mounting debt. Much effort will be expended, but the goal remains distant.

In some cases I think the debt metaphor works. However, as with all abstractions, it leaks. I’d like to bring attention to the situations where the metaphor is a poor one. In many cases a construction analogy captures the business implications better than tech debt.

It’s worth noting that Ward Cunningham thinks his metaphor has been misinterpreted.

> A lot of bloggers at least have explained the debt metaphor and confused it, I think, with the idea that you could write code poorly with the intention of doing a good job later and thinking that that was the primary source of debt.  
> I'm never in favor of writing code poorly, but I am in favor of writing code to reflect your current understanding of a problem even if that understanding is partial.
> 
> — Ward Cunningham

Source: [Video](https://www.youtube.com/watch?v=pqeJFYwnkjE) [Transcript](http://wiki.c2.com/?WardExplainsDebtMetaphor)

Many developers think tech debt is any shortcut that lets you ship sooner. As such they produce shoddy work to meet deadlines, and then use the debt metaphor as a defense. With this framing they can make it seem as the natural course of business. I hope to demonstrate the harm misused metaphors can cause, and propose a more accurate one to use instead.

## Where it leaks

Finance is a zero sum game. Debt is a liability for one person and an asset to another. With financial debts there is an obligation to pay the lenders. Otherwise the borrower’s credit will be tarnished and collectors may pursue them. Since failure to pay debts harms the issuer of that debt I think its right that repayment takes on a ethical quality. Debt is an agreement to pay back the money owed plus interest at a future date.

Tech debt, unlike financial debt, is an asset to no one, it’s only a diminishment of value. This means no one will come to collect. If the technical debt is contained to an area of the code base that is adequately serving its purpose, then not paying is a viable strategy. Imagine having a loan with 0% interest, amortized forever, and no penalty for defaulting — you’d be crazy paying it off.

A metaphor of debt causes an emotional reaction against whatever is labelled as debt. While being an an admirable trait when it comes to money, the sentiment is misplaced in software. Refusing to pay tech debt has none of the serious consequences not paying monetary debts carries. Very often tech debt is brought up as an argument for prioritizing certain work. This will typically imply that the debt will eventually need to be paid off. This alone is a poor reason to make an investment in its repayment to me.

## Where it holds

Naturally a metaphor couldn’t have become so popular without having at least some merit. Personally, I think the debt analogy is best applied to operational inefficiencies where we can’t avoid paying the cost.

For example, consider having many manual deployment steps for a release. Every time the team releases, someone will have to spend time to go through the steps. Automation will take an investment many times greater than a single manual deployment. In this case we can measure how much time we will save against how much time we expect automation will take to get a clear idea about the return on investment. Even here the debt analogy shows its cracks, we can’t be sure how long the work will take before doing it, an estimate is the best we can do. With money we should know exactly how much we owe.

The opportunity cost of an employee’s time should exceed what the amortized fully loaded salary suggests. Experienced and trusted members of the team will be burdened with the cost of deployment. This prevents them from doing high leverage activities, like training, coding, and making decisions. This opportunity cost must be greater than the monetary cost or else the employee is a bad investment. Think about this.

I agree with the sense Cunningham used the term. Its better to release something with imperfect understanding, get feedback, and incorporate that into future releases. If it turns out the domain was modeled incorrectly it may need refactoring. Failing to rearrange the code will cause further development efforts to be inefficient, much like trying to build up savings while paying high interest debt.

He also coined the term when working in a financial domain, since debt is a term in that domain’s ubiquitous language, it made for a natural analogy. I think a better analogy can be had with construction.

## A new analogy

Refactoring is needed as the project evolves in orders of magnitude. I would liken it to building a small building, and then adding rooms on until you have a not so small building. There comes a point where the original floor plan is no longer suitable, and restructuring is called for. If you keep on making additions to a building, it may end up with a weird floor plan, making further additions difficult and costly. When this happens, instead of simply adding rooms, it may be necessary to take down some walls, to reach a better design for the growing scope of a project. This involves deleting code, which many coders delight in. Good planning will prevent the load bearing walls being the ones you have to destroy.

Paying down tech debt is necessarily destructive to previous work, this is something the debt analogy fails to capture. The need for refactoring is to be expected if the project has changed on an order of magnitude since its inception. A design that works for a small project won’t always work for a larger version. In certain situations a renovation is more valuable than additional floor space. If new additions are added onto the old design will also need to be reworked. Many projects will continue to add rooms until they have a big ball of mud.

Not all tech debt is equal. Some will involve relatively small changes and make a big difference to the overall quality of the project. Other forms are more like a bad foundation, where the efforts to remediate prior work will be large. Skilled design will ensure the load bearing foundation won’t need modification.

The more nefarious version of tech debt lies in recently completed work. This is like a contractor who botches a job in an attempt to make a deadline. People responsible for projects don’t always know how to read code, which makes their job of judging quality difficult.

Less professional developers take advantage of this, providing fast installations, that ends up making future work harder. Imagine making a frame on a crooked foundation. Most people will be upset they have to do more work at the shortcomings of another. Once a selfish attitude is adopted by a team, morale, quality, and velocity all suffer.

Of course not all features need to be perfect before they are released. Opening up a room to the public without all the finishing touches is different than something being done poorly. Adding finishing touches, and rearranging things as the software sees real traffic is encouraged. What is appropriate for the project is a hard judgement call.

### Feature development with debt

#### Video Summary

Hal is going to replace a lightbulb, when he goes to get it a shelf breaks. To fix the shelf he gets a screw driver from a drawer that squeaks. He gets oil for the drawer to find out its empty. To get more he tries to start a car that fails to turn over. As he goes to fix the car his wife comes home and asks if he can change the light bulb. He gets out from under the car, shouting: “What does it look like I am doing?”

This captures the feeling of working in a code base that has incurred tech debt. If Hal made a bigger mortgage payment, would any of his difficulties been avoided? This is why I like a construction metaphor over a financial one for software development. The reality of working on systems can’t be captured with a number.

## What to do

I think changing the metaphor of tech debt can improve developer-product manager relations in a few respects.

For developers, it can be helpful to realize there is no ethical obligation to pay tech debt. Tech debt should also never be used to excuse sloppy work with the intention of cleaning it up later. This later often becomes never, and this causes the team’s velocity to be hampered for an individual’s benefit.

If you are managing developers you should consider how the phrase “tech debt” is being used. Sometimes the metaphor refers to a deeper issue within a team.

If the product has recently underwent large changes and rapid growth, then a refactor maybe warranted. Its generally better to do this sooner than later, as more features will mean it will be harder to do later. If these rearrangements aren’t done, then new features will be grafted on in a grotesque manner, making it difficult to modify later. In this case I would recommend talking to the tech lead to figure out why the old design is no longer correct, what the new design is going to be, and the work required to make the change happen.

When the term tech debt is referring to processes that can be improved via automation, this is relatively straight forward to prioritize. Consider the implementation time compared to the time saved to get a sense for the ROI. This can then be used to compare to the rest of the backlog items. Very often these sorts of things will become more valuable with scale. As the team becomes larger the time savings become greater, and these improvements should be revisited every so often. A week of implementation time might pay for itself in a couple of months in terms of time saved.

If the term tech debt is being used in the context of a feature that was recently being developed it can indicate a lack of skill or professionalism from developers. This requires a judgement call from someone who has the owner’s interest in mind, combined with the skill and context to make a good assessment. Addressing these type of issues sooner than later is important, since it will set the tone for the rest of the project. Once people see poor quality work is accepted they too will begin to take shortcuts. Tech debt was never meant to excuse this behavior.

## Conclusion

Tech debt maybe a well known metaphor, but leaves much to be desired. The common interpretation has deviated from its original intention. Refusing to pay financial debt has ethical implications that refusing to pay tech debt doesn’t have. Paying off tech debt generally involves redoing previous work, destroying previous investment. Often the term tech debt is used to refer to rushed implementations that frustrate future efforts. This may arise from trying to meet tight deadlines, a lack of skill, or plain old laziness. While a [mess is not debt](https://sites.google.com/site/unclebobconsultingllc/a-mess-is-not-a-technical-debt), the terms are commonly conflated in industry.

The more general lesson here is that the metaphors we use have consequences. Any time we speak of something in terms of something else, there will be a verbal baggage that gets dragged along. Bad metaphors may cause bad decisions and should be adopted with care.

