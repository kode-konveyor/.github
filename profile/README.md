# Making coding a real profession, producing rock solid code, accessible for people with average level of skills, while Coders can choose where, what, and how much are they work.

## Wait, programming is a real profession, innit?

One definition of a profession is that it is something which have the rules of profession, which make sure that it is hard to screw up if you follow them.

Well, programming/software development/name it as you like is something a lot of us do. And we cannot even agree on its name, much less how to do it.
For example some say TDD is an essential ingredient, but most of the people doing this art do not consistently do it. Even some of those who say it is important.
Sure, there are some broad principles like SOLID, and Clean Code, but they often disregarded, and they often conflict each other in face value.

And anyway, the title is about coding (for now), see below.

## Rock solid code?

Most of the development projects end up as a complete disaster.
Usually it becomes apparent at delivery time.
But even those which start out nicely, accumulate so much rust with time that they become exponentially more hard to push further.
But at least they are just programs, no life depends on them.

Except when it does. Hundreds of people died in the 737Max disasters.

The Kode Konveyor process uses very strict rules, where it is impossible to submit code which is not thoroughly tested (100% mutation coverage!),
the different abstraction layers of the design are consistency checked with themselves and the adjacent layers including the tests and the code.
This naturally lead to a kind of design approach which is now hyped with the name of Domain-driven design.

The design constraints enforce the SOLID principles, with sane decisions about their conflicts, made at metamodel design time.
This is supported by the strictest known CI of the world.
Because of the mutation coverage check, the static analyzer enforcing clean code, and the inter-level consistency checks, no rust can accumulate in the project:
everything in it have a clear purpose, traceable back to the high level business requirements.

The whole process conforms to most of the Common Criteria Evaluation Assurance Level 6 criteria.
The exceptions are that this process does not require formal security policy model, independent testing  and vulnerability analysis.
For comparison, EAL4 is said to be "the highest level at which it is likely to be economically feasible to retrofit to an existing product line",
and the only higher level is EAL7, where the design must be fully formal, and the code must be formally verified.

### Ho-ho, 100% mutation coverage? Are you kidding?

I kid you not. The code layout standard is specifically designed to make it possible. No need to use non-testable constructs for the Coders.
Those are mostly eliminated, and the very few remaining things are moved out of scope, as part of the standard nonmodified project boilerplate.

## Everyone can be a programmer with some learning, no?

Well, everyone can be a bad one.
An average programmer have to understand the business they write the program for,
keep lots of states in the head, know a lot of tools and libraries - which constantly change -
communicate well with the colleagues, and know the Hitchhiker's Guide To The Galaxy by heart.

I might added a nonessential skill here, but be assured that I have left out a lot others needed.

Not everyone have the background to be able to learn new things every day, concentrate deeply for extended periods of time and be able to connect on the personal level right after that.
Probably no one have all the skills which would be needed.

Actually a profession is usually needs creativity in one (or often zero) areas. Traditional programming have a lot of different areas, where different kind of creativity is needed.

Our end goal is to cover all of them with a profession with its own rules, but first let's stick to coding.

### Okay, what is coding then?

Coding is the part where you turn a lot of very small behaviours into tests and code, where the interfaces are formally defined, while the behaviours are described in human language.

The creative part is to turn that human language to test cases. (Writing the tests after that is mechanical, an IDE with good refactors does most of it for you, and probably soon will be entirely done by AI.)

## Coders can choose where, what and how much? It is anarchy!

Well, those small behaviours are ... small, so coding one needs very short time,
the resulting code can be merged without conflicts,
no need for communication between Coders, very little between the Coders and reviewers, so if enough Coders work on a project, 
its speed will follow the average activity level of people.
Maybe slowing down at weekends and holidays, but the project will roll forward.

Actually when we tested out the approach there were times the Coders ate the tasks faster than we could design them.

### Aha! Here is the catch! Code merged without conflicts? No need for communication? It is impossible.

The code layout standard is designed in a way - by heavy use of dependence inversion - that there are very few places where conflict is even possible, 
and those places are essentially lists of items with clear rules of ordering, so conflicts can be automatically solved.

Remember the part about professional rules?
The tasks given to the Coders are defined to the level that there are no real room for misunderstandings,
and the standards of the resulting code are so strict that every single aspect can be automatically checked,
so the Coder gets the feedback from the static code analyzer in the IDE, and the CI.

As the creative part of the coding is translating the behaviour description to tests, it is the only place where there can be place for communication.
But the tasks are very small, specifying the behaviour of corner cases is the job of the low-level designer (who creates those tasks).
Well, the Coder is motivated to find more corner cases (see quality), as paid by the number of test cases, but if those do not conflict with the specification of the LLD, then will be accepted.
The only room for misunderstanding here is by different interpretations of the same written sentence, but as the concepts of the project and the intent of the code is thoroughly and semiformally defined, this room is rather small.

## This coding thing... You kill the creativity from programming. As a programmer I hate it!

Well, we do, and you have every right to not like it.

Coding is admittedly less creative than programming.

In the same way as building cars became much less creative when Ford started to use a production line with a conveyor belt (this is where our name came from). 
Before that you needed a couple of very good engineers to build a car. After that a couple of less qualified people could do the same.

And the engineers could concentrate on the real creative work of designing the cars. And Ford gave good salaries to the workers, and provided them with other rights.

Kode konveyor gives the Coders the freedom of where, when and how much, and we fully intend to build functionalities to the portal which enables Coders to effectively organize.

Because we believe not just that this approach revolutionizes the software industry, but want to stay on the edge of the wave. And the strategy for that is that we provide the best environment for the Coders, so they do not want to work at other places.

## Okay, you were talking about Coders, but they do a small subset of the programming work, what about the others?

We have already tested the whole process, so we have some understanding of what is involved. We identified some professions. We named them Business Analyst, Low Level Designer, Coder, Reviewer and Graphics designer.

We intend to handle those professions in similar way as coding, defining them around exactly one creative step, with thoroughly defined rules. As we already have the consistency checks in the model, some of that already have a draft definition.

But it is a huge work, involving a lot of trial and error. Coming up with just the backend part of coding with a wireframe of the supporting tools (it works, but not great) took most of a year. We expect similar pace with the other professions.

## Eww, this smells waterfall!

Not at all.
Thorough design does not mean a waterfall approach.
You can still go agile, with small fast iterations on all design levels.
You just have to keep those small iterations consistent.
To facilitate this, the model contains milestones, making it possible to suppress errors for things not yet existing on lower levels.

Actually the process design was heavily built on the Agile Architecture approach. for example this is why we generate the documentation from the architecture model and the test case descriptions.

## There must be same drawbacks!

Yes. The process can handle usual greenfield business applications, with the backend using Java/Spring, and the frontend using TypeScript/Angular (on platforms supported by cordova).

There are only a few ecosystems which have the basic tooling needed for it, and figuring out the ecosystem-specific rules, and supporting them with technology is a great work.
Python, C#, C++ and probably a very short list of other languages have the potential to be covered.

Applying the process for embedded systems would need translators to weed out the DI which is an integral part of the approach.
Also, there are numerous design decisions preferring maintainability over performance.
For a usual business application this is no problem, the critical parts can be handcrafted and used as libraries.
But it can be showstopper for an embedded system.

There are application domains for which this approach is not adequate. You probably do not want to use it for number crunching, AI, and system programming. But probably it is okay for their user/management interface.

## I love this, where can I start working as a Coder (Business Analyst, Low Level designer, Reviewer)/ will you take and develop my project?

There are a lot of work ahead yet.
A lot of things have yet to be figured out, developed and corecctly rewritten.
Probably we will be able to start some projects soon as learning exercises, but probably the first ones will be open source ones, and the portal itself supporting the process.

