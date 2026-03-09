# Exercise 11.1 – CI/CD Discussion

For a Python-based project, the typical CI pipeline involves three core steps: linting, testing, and building.

**Linting** is commonly handled by tools like *Flake8* or  *Pylint* , which enforce style conventions and catch potential errors early. *Black* is also widely used as an opinionated auto-formatter that removes debates about code style entirely.

**Testing** in the Python ecosystem is dominated by  *pytest* , which is flexible, well-supported, and easy to integrate into any CI workflow. For measuring test coverage, *pytest-cov* is the standard companion. For more complex projects, *tox* can help run tests across multiple Python versions.

**Building** Python projects typically involves tools like  *setuptools* ,  *poetry* , or *build* (PEP 517). Poetry in particular has become popular for managing dependencies and packaging in one tool.

Beyond Jenkins and GitHub Actions, there are several solid CI/CD alternatives. **GitLab CI/CD** is tightly integrated with GitLab repositories and is a strong choice if the team already uses GitLab. **CircleCI** and **Travis CI** are mature cloud-based options with straightforward YAML configuration. **Bitbucket Pipelines** works well for teams using Atlassian products, and **Azure DevOps Pipelines** is a natural fit for Microsoft-centric environments.

As for self-hosted vs. cloud-based: for most small-to-medium teams, a **cloud-based** solution is preferable. It removes the overhead of maintaining infrastructure, scales automatically, and gets you up and running quickly. A self-hosted option like Jenkins makes more sense when there are strict security or compliance requirements, access to private internal resources is needed, or the team has DevOps capacity to manage the setup. The decision really comes down to team size, budget, and how much control over the environment is needed.
