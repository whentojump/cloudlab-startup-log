# Profile for Acto on CloudLab

## Usage

### Fetch the profile

First, obtain the profile, by either accessing this link https://www.cloudlab.us/p/Sieve-Acto/acto-cloudlab?refspec=refs/heads/main, or creating a new one from this repository following the instructions below:

<details><summary>Import profiles from repository</summary>

On the web dashboard of CloudLab, click "Experiments" -- "Create Experiment Profile"

1. Give your profile a name, e.g. `acto-cloudlab`.
2. Click the "Git Repo" button and enter the URL `https://github.com/xlab-uiuc/acto-cloudlab`. "Confirm".
3. Preview the information loaded from the repo, e.g. source code, description, instructions etc.
4. Optionally configure the permissions as per your needs. "Create".

After the creation procedure is done, click the "Instantiate" button.

</details>

### Instantiate the profile

Either way, you should now be landing on the page of instantiating the profile, i.e. create an experiment based on it.

1. **Select a Profile**: This profile (`acto-cloudlab`, or your provided name if you manually imported it) should be automatically selected. You may want to read the description on screen.
2. **Parameterize**: Choose the hardware type. The default value `c6420` is recommended for the best reproduced results. However, if that type is not currently available, you may choose another one. Check the current resource availability on [this page](https://www.cloudlab.us/resinfo.php).
3. **Finalize**: Optionally give your experiment a name. If you are a member of multiple CloudLab projects, choose the proper one for running the experiment also on this screen.
4. **Schedule**: Generally you would leave this screen as default and extend the experiment afterwards if needed. Click the "Finish" button.

Wait for the experiment to be created and set up. **Note that there can be such a stage where the progress bar indicates completeness, but the "State" is `booted (startup services are still running)`. Please be patient and wait for "State" to become `ready`** -- because at this time, the machine is still running the [startup scripts](scripts) and the environment isn't fully set up yet.

Once the startup scripts also completes, you can log in to the machine and begin your tests.

## Development

- When this repository gets updated, the imported CloudLab profile won't synchronize automatically. You should:
    1. Go to "Experiments" -- "My Profiles" and find the profile.
    2. Click the edit icon.
    3. Click the "Update" button next to the field "Repository".
    4. When it gets done, verify that the commit hash is the desired value.
- Some of the internals were discussed in https://github.com/xlab-uiuc/acto/pull/257.
