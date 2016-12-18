- cognitive bias

- talk is about making UI (GUI)

- data binding
    
    - data binding binds UI elements to an application domain model
    
    - observer pattern
    
- How do we perform?

    Until recently, most JS frameworks concentrated on the first problem, either by making the DOM easier to navigate (jQUERY), or by tying the elements to controller objects which take responsibility for keeping them up to date (BackBone, angular etc).


- Object.observe
    (Simplifies binding
    MUTABLE DATA
    — to a —
    STATEFUL DOM)

- functional programming
    Just a trend
    assuming it's the way to go
    Why OO was popular?
    Reason 1 - It was thought to be easy to learn.
    Reason 2 - It was thought to make code reuse easier.
    Reason 3 - It was hyped.
    Reason 4 - It created a new software industry.
    - minimise the nuisance of state
    object oriented programming, Joe Armstrong:
    The problem with object-oriented languages is they’ve got all this implicit environment that they carry around with them. You wanted a banana but what you got was a gorilla holding the banana and the entire jungle.
    //- You wanted a banana but what you got was a gorilla holding the banana and the entire 
    jungle
    the industry started realising the mistake
    http://harmful.cat-v.org/software/OO_programming/why_oo_sucks

- immutability, 
    immutable.js
    MVC


- dom is mutable though. is a big problem because: 
    - browser idiosyncrasies/incompatibilities
    - (modifiying/querying is slow)

- what if we treat the browser as rendering layer?
    What if we could write our templates as plain JavaScript functions that take in our current application state and return a visual representation for that state?
    render(data) -> html

- virtual-dom (stateless-dom)

- react 
- a js library for building UI
    
    - Declarative (Instead of low-level techniques like traversing the DOM tree manually, you simply declare how a component should look like.)
    
    - Component-Based (stateful)
    
    - Learn Once, Write Anywhere (react native, desktop applications, watch)

- “Simply express how your app should look at any given point in time, and React will automatically manage all UI updates” (essentially stateless dom)
Creating a virtual DOM in JavaScript is cheap compared to manipulating the DOM directly. (https://gist.github.com/Raynos/8414846)

It’s hard to beat the simplicity of a system like this. In many cases, the view code is simply a function which takes data and returns DOM (or at least, Virtual DOM). It’s stateless and declarative. Until you need a bit of state, that is, which React can also handle. Today, I can’t imagine using anything else.

- OM


- react + clojurescript (can do fast reference equality checks because data structures won't change)
    ENTIRE UI STATE
    — in a —
    SINGLE, IMMUTABLE OBJECT
    “THE FUTURE
    — of —
    JAVASCRIPT MVCS”
    https://circleci.com/blog/why-we-use-om-and-why-were-excited-for-om-next/

- We'll see how, perhaps unintuitively, immutable data allows a new library, Om, to outperform a reasonably performant JavaScript MVC like Backbone.js without hand optimization from the user. Om itself is built upon the absolutely wonderful React library from Facebook. If you haven't checked it out before, I recommend watching this video from JSConf EU 2013. Interestingly because of immutable data Om can deliver even better results than using React out of the box

- outperforms any JS MVC framework (like Backbone.js)
    “If you treat the browser as a remote rendering engine and stop treating it as a place to query and store crap, everything gets faster.”
    UNDO FOR FREE
    EXPORT STATE

- in a parallel world, Evan's story

- Is the future rendering IMMUTABLE DATA — to a — STATELESS DOM?

- (probably not, there will be something better in the future)

- keep an open mind
