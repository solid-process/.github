<p align="center">
  <img src="https://raw.githubusercontent.com/solid-process/the-assets/main/images/png/solid-process_sticker_a01.png" alt="Solid Process" width="300" />
  <br />
  <strong><em>Write business logic that scales.</em></strong>
</p>

Solid Process is where the **`business rules`** of a Ruby or Rails app go to **`stay legible`**. Each library does one job, composes with the rest, and keeps the same shape whether you're writing a single service or wiring up a whole domain.

As more of that code gets read and written by AI agents, **`the structure that keeps a process clear for a teammate`** is the same structure that **`keeps it cheap for an agent to reason about`**.

> _Make it **`work`**;<br/>
> Make it **`better`**;<br/>
> Make it **`even better`**;<br/>
> Without throwing away what came before._

## Featured

### ⚛️ [solid-process](https://github.com/solid-process/solid-process)

It is a Ruby/Rails library that **`encapsulates business logic into manageable processes`**. It simplifies writing, testing, maintaining, and evolving your code, so it stays clear and approachable as your application scales.

Write a process as a single object with typed input, an ordered set of steps, and a result. From that one shape you get:

1. Composition
2. Nested processes
3. Database transactions
4. Built-in instrumentation
5. All without fighting Rails conventions

It's the evolution of [`u-case`](https://github.com/serradura/u-case), with fewer compatibility constraints and everything learned from running it in production.

### 🔀 [solid-result](https://github.com/solid-process/solid-result)

A general-purpose result object: `Success(...)` or `Failure(...)`, with hooks and pattern matching for reacting to an outcome. It's how `solid-process` represents every result, and it stands on its own to bring [Railway-Oriented Programming](https://fsharpforfunandprofit.com/rop/) to any Ruby code.

### 🧩 [solid-adapters](https://github.com/solid-process/solid-adapters)

Interface contracts in pure Ruby. Declare the boundary an object has to honor, wrap a concrete implementation in a checked proxy, and keep your ports and adapters honest, with no Rails in sight.

## Learn by example

**`"Talk is cheap. Show me the code"`**, as Linus Torvalds put it. So here are two repositories instead of an argument.

They are the same application built at many levels, from a fat controller all the way to ports and adapters. I built them because the loudest opinions in this space usually arrive with no working example attached: that Rails alone is always enough, or that you always need a hexagon around it. Read the diffs and weigh the cost for yourself.

### ✨ [solid-rails-app](https://github.com/solid-process/solid-rails-app)

The same app climbing across twelve branches, from simple service and form objects up to a full ports-and-adapters (hexagonal) build with `solid-process`. It shows what the gem buys at each step, and where stopping early is already a production-ready win.

### 🚆 [rails-way-app](https://github.com/solid-process/rails-way-app)

The same Web and REST API app in eighteen versions, each one getting more out of plain MVC and the Rails Way, no gems required. Every version reports its lines of code and Rubycritic score, so a refactor's cost is a number, not a feeling. It is the baseline for how far convention alone carries you, and the idea keeps going, pushed further still, in [Rails Whey](https://github.com/railswhey/app).

## How we think about it

A few rules shape the libraries:

1. **One library, one job.** `solid-result` represents outcomes, `solid-adapters` guards boundaries, `solid-process` orchestrates steps. Reach for only the part you need.
2. **Build on Rails, don't reinvent it.** `solid-process` is built on ActiveModel and ActiveSupport on purpose, reusing Rails' own building blocks instead of reimplementing them. That's a deliberate break from `u-case`, which stayed Rails-optional.
3. **Readable as it scales.** A process should be as easy to follow in year three as on day one, for whoever (or whatever) reads it next.
4. **Pragmatic, not dogmatic.** Adopt it where it fits and leave the rest as vanilla Rails. The goal is the right tool for the job, not architecture for its own sake.

## Lineage

These libraries grew out of [`u-case`](https://github.com/serradura/u-case) and the [μ-gems](https://github.com/u-gems) collection, an earlier set of small Ruby libraries with a functional heart. `solid-process` keeps that goal, folding in everything learned from years of use in production across many companies.

`u-case` is not going anywhere: its public API is frozen and stays supported, so apps that depend on it keep working untouched. `solid-process` is the place where the abstractions get rethought without that constraint. If you're happy with u-case, stay; if you want the next-generation ideas, they live here.

## Links

- 🌐 Website: https://solidprocess.dev
- 🎨 Brand assets: https://github.com/solid-process/the-assets

## License

Each project ships under its own MIT license. Check the repo for details.
