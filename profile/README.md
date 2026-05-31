<p align="center">
  <img src="https://raw.githubusercontent.com/solid-process/the-assets/main/images/png/solid-process_sticker_a01.png" alt="Solid Process" width="300" />
  <br />
  <strong><em>Write business logic that scales.</em></strong>
</p>

Solid Process is where the business rules of a Ruby or Rails app go to stay legible. Each library does one job in plain Ruby, composes with the rest, and keeps the same shape whether you're writing a single service or wiring up a whole domain.

> _Make it work, make it better, make it even better, without throwing away what came before._

## Featured

### ⚛️ [solid-process](https://github.com/solid-process/solid-process)

`solid-process` is a Ruby/Rails library that encapsulates business logic into manageable processes. It simplifies writing, testing, maintaining, and evolving your code, so it stays clear and approachable as your application scales.

Write a process as a single object: typed input, an ordered set of steps, and a result that's either `Success(...)` or `Failure(...)`. From that one shape you get composition, nested processes, transactions, and built-in instrumentation, all without fighting Rails conventions. It's the evolution of [`u-case`](https://github.com/serradura/u-case), with fewer compatibility constraints and everything learned from running it in production.

### 🔀 [solid-result](https://github.com/solid-process/solid-result)

A general-purpose result object: `Success(...)` or `Failure(...)`, with hooks and pattern matching for reacting to an outcome. It's how `solid-process` represents every result, and it stands on its own to bring [Railway-Oriented Programming](https://fsharpforfunandprofit.com/rop/) to any Ruby code.

### 🧩 [solid-adapters](https://github.com/solid-process/solid-adapters)

Interface contracts in pure Ruby. Declare the boundary an object has to honor, wrap a concrete implementation in a checked proxy, and keep your ports and adapters honest, with no Rails in sight.

## Learn by example

### ✨ [solid-rails-app](https://github.com/solid-process/solid-rails-app)

The same kind of app with `solid-process` folded in across twelve branches, from simple service and form objects up to a full ports-and-adapters (hexagonal) build. It shows where the gems earn their place, and where stopping early is already a production-ready win.

### 🚆 [rails-way-app](https://github.com/solid-process/rails-way-app)

The same Web and REST API app built in eighteen versions, each step getting more out of plain MVC and the Rails Way. Every version reports its lines of code and Rubycritic score, so you can see exactly what a refactor buys. This is the baseline: how far convention alone carries you before you reach for anything else.

## How we think about it

A few rules shape the libraries:

1. **One library, one job.** `solid-result` represents outcomes, `solid-adapters` guards boundaries, `solid-process` orchestrates steps. Reach for only the part you need.
2. **Build on Rails, don't reinvent it.** `solid-process` is built on ActiveModel and ActiveSupport on purpose, reusing Rails' own building blocks instead of reimplementing them. That's a deliberate break from `u-case`, which stayed Rails-optional. (`solid-result` and `solid-adapters` are the standalone pieces: pure Ruby, no framework attached.)
3. **Readable as it scales.** A process should be as easy to follow in year three as on day one. The structure that keeps it legible for the next person is the same structure that makes it cheap for an AI agent to reason about.
4. **Pragmatic, not dogmatic.** Adopt it where it fits and leave the rest as vanilla Rails. The goal is the right tool for the job, not architecture for its own sake.

## Lineage

These libraries grew out of [`u-case`](https://github.com/serradura/u-case) and the [μ-gems](https://github.com/u-gems) collection, an earlier set of small Ruby libraries with a functional heart. `solid-process` keeps that goal, folding in everything learned from years of u-case in production across many companies.

`u-case` is not going anywhere: its public API is frozen and stays supported, so apps that depend on it keep working untouched. `solid-process` is the place where the abstractions get rethought without that constraint. If you're happy with u-case, stay; if you want the next-generation ideas, they live here.

## Links

- 🌐 Website: [solidprocess.dev](https://solidprocess.dev)
- 🎨 Brand assets: [the-assets](https://github.com/solid-process/the-assets)
- 👥 Community: [Ada.rb](https://adarb.org)

## License

Each project ships under its own MIT license. Check the repo for details.
