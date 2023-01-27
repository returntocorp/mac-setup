# mac-setup

Martin's scripts to set up a MacOS host on AWS/EC2.

Approximate steps to get started:

1. [Set the shell to Bash](https://aws.amazon.com/premiumsupport/knowledge-center/ssm-session-manager-change-shell/)
2. Log in with: `aws ssm start-session --target i-XXXXXXXXXXXX`
3. Clone this repo: `git clone https://github.com/returntocorp/mac-setup.git`
4. Run the setup script: `./mac-setup/scripts/setup-all`
5. Fix problems. Log out/in as needed.
6. Clone the semgrep repo or other repos of interest. For accessing
   private repos, the recommended way is to obtain read-only
   permission via a repo-specific
   [deploy key](https://github.blog/2015-06-16-read-only-deploy-keys/).
   * Create a key pair on the client side using `ssh-keygen` if there
     isn't one already in `.ssh/`.
   * Go to the private repo of interest and add the public key to
     the authorized Deploy Keys.
