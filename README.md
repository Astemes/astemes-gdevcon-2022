# astemes-gdevcon-2022
Supporting material for the presentation "Unit Testing From the Trenches" held during G-DevCon 2022 in Amsterdam.

The purpose of the presentation was to share some real world experience and anechdotes of using Test Driven Development and Design (TDD).
For a demonstration of what the workflow looks like writing tests first, please see the demonstration [here](https://youtu.be/cgOtv9jrpvc).

The slides from the presentation are availble [here](https://github.com/Astemes/astemes-gdevcon-2022/blob/main/Presentation/Unit%20Testing%20from%20the%20Trenches.pdf).

To run the unit tests you will need LUnit Unit Test Framework available [at VIPM](https://www.vipm.io/package/astemes_lib_lunit/).

## Addendum

A few additions and comments which came up in discussions after the presentation.
Thanks for great discussion and feedback Casey, Christian, and others.

- I use [LUnit](https://www.vipm.io/package/astemes_lib_lunit/) as unit test framework, but the ideas in the presentation should be tool agnostic.
- In the low level PSU example, the idea is that we are develping the code to interface with the hardware by reading from and writing to the instrument. What we are interested in testing is that the messages are formated and parsed correctly. We can then hopefully thrust that VISA (or whatever driver layer you might be using) will take care of the low level communication.
- Unit tests can not replace system level tests, and I am not proposing that we replace all our testing with TDD style unit testing. What I am trying to say is that it is much more convenient to solve any issues (*i.e.* find bugs) locally by testing the subunits of a system than it is to test through the whole system by hand (*i.e.* debugging). 
- For doing unit testing in the way proposed, it is almost a hard requirement to use object oriented LabVIEW. The reason is that abstract classes and interfaces are the easiest way to create abstractions, which can then be mocked or stubbed.

## Where to go from here

To learn more on this topic I'd have a few suggestions. Please feel free add more and create a pull request. 

You can always reach out to me directly to discuss more on this topic, I'm keen to talk and learn. 
As I am an independent consultant, it is also rather easy to setup pair programming sessions (either in person or online) where we work on your code using TDD.
I think this is a great way of learning the mindset and getting into the flow.

- Have a look at the youtube video [demonstration of the TDD workflow](https://youtu.be/cgOtv9jrpvc). If you like it, do let me know so I know if I should produce more content.
- For an introduction to unit testing in general and the tools available in LabVIEW, I made a presentation during GLA Summit. This is available [here](https://www.youtube.com/watch?v=Kys_w2RNffw&t=1111s).
- Within the LabVIEW world I have not seen a lot of content on this topic. Sam has some great posts on [his blog](https://blog.sasworkshops.com/) which are worth reading.
- Outside the LabVIEW world there is a lot of good stuff and TDD is much more common. I would recommend material for java or C# as the patterns tend to be most similar to what can be done in LabVIEW. 
- You can also have a look at my other repositories at [GitHub](https://github.com/astemes). They are all open source and developed using TDD. A good starting point is the [examples](https://github.com/Astemes/astemes-triarc-examples) for our application framework. These are all developed using TDD with the tests in the repo and it should give an idea of what it may look like.

Thanks again for the interest and please let me know if you find this helpful or if you have suggestions.
Any feedback will directly impact future topics I might bring up with the community, so thanks in advance.
