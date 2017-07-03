# Contribution Guidelines

I would recommend using [Zenhub](https://www.zenhub.io/) if you can, as the pipelines are quite useful. If you can't afford it (due to having it as a private repository), then vanilla issues can suffice, you'll just need to create some additional labels to replace `Icebox`, `Review` etc.

1. Create an issue with the `MVC` of your project idea.
2. Add relevant labels to the issues, including, but not limited to:
  - Department
  - Categorie(s)
  - Proposal
3. Tag relevant people to comment on the proposal, this could be members of the team that would need to do the work, project managers, engineering managers etc. You can use `@person` in a comment to flag their attention.
4. Enjoy the discourse as your proposal is discussed, until it reaches one of three stages:
  - Won't do
  - On Ice | Hold
  - Submit 2 Pager

If your project reaches the `Submit 2 Pager` phase, then it's time to create a new branch off of `master`, idealy `$(whoami)-{ProjectName}`, make a copy of the [Project Template](Templates/Project.md), and add it to the `Projects/{TEAM}/Ideation` directory and fill in the relevant information.

Once your *2 Pager* is complete, push your changes and open a Pull Request for Peer Review. On your Pull Request page, you can request Reviewers, so tag the relevant people that need to be aware of the proposed project, so that they can comment on the minutiae of the plan.

Once the *2 Pager* is accepted, and timelines have been decided, `git mv` it to the `Projects/{TEAM}/Formalised` directory, and update the `Projects/{README.md,TEAM/README.md}` to include the new project information, and close the initial Issue that was created.
