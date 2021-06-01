+++
title = "Three Components for Reviewing a Pull Request"
outputs = ["Reveal"]
+++

# Three Components for Reviewing a Pull Request
Thomas J. Fan

{{< social >}}
{{< talk-link data-umbrella-2021-reviewing-prs >}}

---

## Three Components for Reviewing a Pull Request

{{% grid middle %}}

{{< g 1 >}}

### **Overview**

1. Mechanics
2. Social Aspects
3. Technical Aspects

{{< /g >}}

{{< g 1 >}}

Thomas J. Fan
{{< social >}}
{{< talk-link data-umbrella-2021-reviewing-prs >}}

{{< /g >}}

{{% /grid %}}

---

{{% grid middle %}}
{{% g 1 %}}

# Glossary

- PR: Pull request
- Reviewer: Person reviewing the pull request
- Contributor: Author of the pull request


{{% /g %}}
{{% g 1 %}}

{{< figure src="images/dictionary.jpg" height="500px" >}}

{{% /g %}}
{{% /grid %}}

---

# Why code review? 🔎 💻

{{% grid middle %}}

{{% g 1 %}}
{{< figure src="images/why-review.jpg" height="500px" >}}
{{% /g %}}

{{% g 1 %}}

- Correctness
- Maintainability
- Knowledge sharing

{{% /g %}}

{{% /grid %}}

---

# 1. Mechanics
{{< figure src="images/mechanics.jpg" height="550px" >}}

---

# Mechanics of Reviewing a Pull Request on GitHub 🛠

---

{{< figure src="images/scikit-learn-main.png" width="100%">}}

---

{{< figure src="images/pull_request_list.png" width="100%">}}

---

{{< figure src="images/pull_request_single.png" width="100%">}}

---

{{< figure src="images/pull_request_files_changed.png" width="100%">}}

---

{{< figure src="images/suggestion-dialog.png" width="100%">}}

---

{{% grid middle %}}

{{% g 1 %}}
{{< figure src="images/markdown.png" width="100%">}}
{{% /g %}}

{{% g 1 %}}

{{< figure src="images/markdown-rendered.png" width="50%">}}
{{% /g %}}

{{% /grid %}}

---

{{< figure src="images/numpy-suggestions.png" width="100%" >}}

---

{{< figure src="images/multi-suggestions.png" width="100%" >}}

---

# Demo

---

{{< figure src="images/pull_request_review_options.png" width="100%" >}}

---

# Browsing code in GitHub

- `t`: Activate the file finder
- `l`: Jump to a line in your code
- `b`: Open blame view

---

{{< figure src="images/ci-checks.png" width="100%" >}}

---

# Demo

---

## Overview of Mechanics

- Markdown with some extras
- Use suggestions when possible
- Check and Navigate the CI
- [GitHub Keyboard](https://docs.github.com/en/github/getting-started-with-github/using-github/keyboard-shortcuts#source-code-browsing) shortcuts for browsing code

---

{{% grid middle %}}
{{% g 1 %}}

# 2. Social Aspects

- Collaboration
- Conversational
- Contributor In the Loop

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/collaborate.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

# Ask, Don't Tell

{{% grid %}}
{{% g 1 success %}}
## ✅
This would cause a performance issue. We can cache the results and use it again for sequential calls. What do you think?
{{% /g %}}

{{% g 1 alert %}}
## ❌
Never do this. It is very slow.
{{% /g %}}

{{% /grid %}}

---

# Offer Alternative Implementations

{{% grid %}}
{{% g 1 success %}}
## ✅
This leads to a memory regression. May we try using batched calls to reduce the memory overhead? Something like this:

**Insert code snippet**
{{% /g %}}

{{% g 1 alert %}}
## ❌
This leads to a memory regression.
{{% /g %}}
{{% /grid %}}

---

# Explain why code should be changed

{{% grid %}}
{{% g 1 success %}}
## ✅
We have similar logic in multiple places in this PR. Can we refactor this into its own function to be more DRY?
{{% /g %}}

{{% g 1 alert %}}
## ❌
Please refactor this into its own function.
{{% /g %}}
{{% /grid %}}

---

# Explain why code should be changed

{{< figure src="images/kwargs-explain.png" width="100%">}}

---

# Avoid using derogatory terms

{{% grid %}}
{{% g 1 success %}}
## ✅
We can improve this function by adding more input validation and tests on the following edge cases:

**List edge cases**

{{% /g %}}

{{% g 1 alert %}}
## ❌
This whole function is stupid.
{{% /g %}}
{{% /grid %}}

---

# Be humble
#### **Assume everyone is intelligent and well-meaning**

{{% grid %}}
{{% g 1 success %}}
## ✅
I checked the reference and it uses the following equation:

**Insert Equation**

I do not think this matches our implementation. What do you think?
{{% /g %}}

{{% g 1 alert %}}
## ❌
I have 20 years of experience and this is clearly wrong.
{{% /g %}}
{{% /grid %}}

---

# Ask for clarification

{{% grid %}}
{{% g 1 success %}}
## ✅
This is part of the code is unclear. What was your reasoning behind using a queue here?
{{% /g %}}

{{% g 1 alert %}}
## ❌
This is confusing.
{{% /g %}}

---


# Communicate which ideas you do not feel strongly about

{{< figure src="images/no-strong-opinion.png" width="100%">}}

---

# Communicate which ideas you feel strongly about

{{< figure src="images/strong-opinion.png" width="100%">}}

---

# Try to leave a positive comment

{{% g 1 success %}}
## ✅
This is a very clever usage of `defaultdict`!
{{% /g %}}

---

# Thank contributors for their work

{{% g 1 success %}}
## ✅
Thank you for the PR @thomasjpfan!
{{% /g %}}

---

# General Social Aspects 🎙

- Be explicit
- Do not be sarcastic
- Keep the discussion around the code
- Self-directed commentary: "I feel", and " I think"

---


{{% grid middle %}}
{{% g 2 %}}

## Disagreement

- Inevitable and good: People are engaged
- Keep it positive
- When code gets to a certain level of quality, disagreement is more about tradeoffs.
- Get more opinions: Ping other contributors that are familiar with the code or the subject

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/two-birds.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

{{% grid middle %}}
{{% g 2 %}}

# Talk synchronously
- If there are too many "I do not understand" or "alternative solutions"
- Keep meeting notes and comment on the PR about the discussion

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/laptop.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}


---

{{% grid middle %}}
{{% g 1 %}}

# 2. Social Aspects

- Collaboration
- Conversational
- Contributor In the Loop

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/collaborate.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

{{% grid middle %}}
{{% g 1 %}}

# 3. Technical aspects

- Presentation
- Engineering
- Testing

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/technical.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

# Presentation
### **3. Technical aspects**

{{< figure src="images/presentation.jpg" width="55%" >}}

---

## Does the description describe why the change is being made?
- Matches the contents of the PR

{{< figure src="images/describe-pr.png" width="100%" >}}

---

## Familiarize yourself with the context of the issue and why the Pull request exists.

{{< figure src="images/describe-pr.png" width="100%" >}}

---

## Do we want this new feature? 🤔
- Make sure that the team and the community wants to build the feature
- Every line of code we add means more code size and more maintenance

---

## Was unrelated code changed? 🛠
- Only include files that are directly related to the change

```json
{
    "editor.formatOnSave": false,
}
```

---

{{% grid middle %}}
{{% g 1 %}}

## Is the PR easy to review?
- Difficulty of reviewing a PR scales non-linearly with size
- Suggest how to split the PR into smaller PRs

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/connections.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

## Is the PR easy to review?

{{< figure src="images/super-long.png" width="100%" >}}

**Some PRs must be large because they require major design changes**

---

# Engineering
### **3. Technical aspects**

---

## Every change should be intentional

{{< figure src="images/paperclips-change.jpg" width="100%" >}}

---

## Offer ways to simplify or improve code

{{< figure src="images/offer.jpg" width="70%" >}}

---

{{% grid middle %}}
{{% g 1 %}}

## Was a core component changed?
- Needs to be discussed
- Extra scrutiny

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/needle-core-changed.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

## Does the change maintain backwards compatibility?

{{< figure src="images/puzzle-bc.jpg" width="70%" >}}

---

{{% grid middle %}}
{{% g 1 %}}

## Could the change be more generally applicable elsewhere in the codebase?
- Small changes: encourage the author to make the changes
- Big changes: open another issue to track it

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/nail-applicable.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

## Does the change use idiomatic or existing functionally in the codebase?

{{< figure src="images/tools-exist.jpg" width="50%" >}}

**There could be helper functions already implemented**

---

## Will the change break something planned in the future?

{{< figure src="images/planning.jpg" width="60%" >}}

**It may directly contradict planned future work**

---

## Performance optimizations
#### **Require Benchmarks**
- [memory-profiler](https://pypi.org/project/memory-profiler/)
- [scalene](https://github.com/plasma-umass/scalene)
- [filprofiler](https://github.com/pythonspeed/filprofiler)
- [py-spy](https://github.com/benfred/py-spy)
- [viztracer](https://viztracer.readthedocs.io)

---

{{% grid middle %}}
{{% g 1 %}}

## Is there documentation?
- User guide and documentation
- Audience

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/audience.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

### Application (Examples)
{{< figure src="images/example.png" width="100%" >}}

---

### Understanding (User Guide)
{{< figure src="images/user-guide.png" width="100%" >}}

---

### Details (API docs)
{{< figure src="images/api.png" width="100%" >}}

---

{{% grid middle %}}
{{% g 1 %}}

## Code comments

- Subtle changes
- Are comments out of date?

{{% /g %}}
{{% g 2 %}}

{{< figure src="images/code-comments.png" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

{{% grid middle %}}
{{% g 1 %}}

## Was there a hack?

- Needs to be discussed
- Code comments

{{% /g %}}
{{% g 2 %}}

{{< figure src="images/hacking.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

# Testing
### **3. Technical aspects**

---

{{% grid middle %}}
{{% g 2 %}}

## Are there tests?

- Help tell us if we break something in the future
- Help tell us if the PR is correct
- Bug fixes require non-regression tests: failed before and no longer fails

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/testing.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}


---

## When is it okay not have test? 🧪
- Documentation
- Performance optimizations
- Memory optimizations

---

# Are the tests comprehensive?

{{< figure src="images/airplane-config.jpg" width="60%" >}}

**Test the different options or input types of a function**

---

{{% grid middle %}}
{{% g 1 %}}

## CI test fails what does it mean?

- Can be unrelated
- Can be linting error
- Can be an actual error

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/ci-checks.png" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

{{% grid middle %}}
{{% g 1 %}}

# 3. Technical aspects

- Presentation
- Engineering
- Testing

{{% /g %}}
{{% g 1 %}}

{{< figure src="images/technical.jpg" width="100%" >}}

{{% /g %}}
{{% /grid %}}

---

{{% grid middle %}}

{{< g 1 >}}

# Why code review? 🔎 💻

{{% grid middle %}}

{{% g 1 %}}
{{< figure src="images/why-review.jpg" height="500px" >}}
{{% /g %}}

{{% g 1 %}}

- Correctness
- Maintainability
- Knowledge sharing

{{% /g %}}

{{% /grid %}}

---

## Three Components for Reviewing a Pull Request

{{% grid %}}
{{% g 1 %}}

### **Overview**

1. Mechanics
2. Social Aspects
3. Technical Aspects

{{< /g >}}

{{< g 1 >}}

Thomas J. Fan
{{< social >}}
{{< talk-link data-umbrella-2021-reviewing-prs >}}

{{< /g >}}

{{% /grid %}}
