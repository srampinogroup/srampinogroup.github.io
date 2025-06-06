# Authentication

## Installing `gh`

In order to avoid having to enter credentials on the clusters, this
is what I would do. First, make sure you have an activated
environment. Exceptionally for this case, I would say that installing
in base environment is fine, but you can also install it on every
project (I did not test if you need to re-enter credentials for each
virtual env in that case). So, we can install `gh` without root in
conda like this:
```bash
conda install -y gh
```

Once done (it took a while for me on Avogadro), you can login
permanently with
```bash
gh auth login
```

You will be asked in interactive mode two questions, first "where do
you use GitHub", answer "GitHub.com". Second, "what is your preferred
protocol", choose "HTTPS" (should be default). Confirme with `Y`, and
choose "Login with a browser". If you have forwarded X server, you
will have a remote destop browser opening. If not that is okay, just
open (from anywhere) the URL
```
https://github.com/login/device
```
and enter the code that was given to you by the `gh` utility. Have
your phone near you for the two-factor authentication. And that's it.

Output of whole process should look like this:
![image](https://github.com/user-attachments/assets/8a5129c8-3925-4499-96ce-5ee89bcb1f83)


More info on `gh`: https://github.com/cli/cli
