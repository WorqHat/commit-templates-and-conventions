# GitHub Branch Name and Commit Templates

As a part of our ongoing efforts to streamline our Technical Processes and to make it easier to maintain commit histories over time, there are going to be a few more regulations regarding the Commit Messages and Branch Names

The ability to quickly identify the commit message associated with a line of code, as well as authorship information, is incredibly valuable. Writing good commit messages that clearly explain what the code does makes this functionality all the more helpful.

The Commit Template that we will be trying to use is

```
<type>: <subject>

[optional body in description]

[optional footer(s) in description]
```

## Example

```
fix: prevent racing of requests

Introduce a request id and a reference to latest request. Dismiss
incoming responses other than from latest request.

Remove timeouts which were used to mitigate the racing issue but are
obsolete now.

Reviewed-by: Z
Refs: #123
```

The different variables that can be used as <type> are

`build`: Build related changes (eg: npm related/ adding external dependencies)
`chore`: A code change that external user won't see (eg: change to .gitignore file or .prettierrc file)
`feat`: A new feature
`fix`: A bug fix
`docs`: Documentation related changes
`refactor`: A code that neither fix bug nor adds a feature. (eg: You can use this when there is semantic changes like renaming a variable/ function name)
`perf`: A code that improves performance
`style`: A code that is related to styling
`test`: Adding new test or making changes to existing test

The design team will be focusing mainly on the style tags and the rest of the team will be focusing on build, feat, fix and others.

But please make sure you use the appropriate tags at all times.

A commit body or description is free-form and MAY consist of any number of newline separated paragraphs.
A footer’s token MUST use - in place of whitespace characters, e.g., Acked-by (this helps differentiate the footer section from a multi-paragraph body).

Why we are working on this:

Automatically generating CHANGELOGs.
Automatically determining a semantic version bump (based on the types of commits landed).
Communicating the nature of changes to teammates, the public, and other stakeholders.
Triggering build and publish processes.
Making it easier for people to contribute to your projects, by allowing them to explore a more structured commit history.

Also, we will be following a similar pattern for branch conventions as well:

git branch <category or type/reference/description-in-kebab-case>

Examples:

You need to add or remove a feature: git branch feat/issue-42/create-new-button-component 
You need to fix a bug: git branch fix/issue-342/button-overlap-form-on-mobile
git branch style/no-ref/registration-form-not-working 
git branch test/no-ref/refactor-components-with-atomic-design


We will be discussing these Git Commit and Branch Templates in more detail during our Monday's Standup Meeting.
