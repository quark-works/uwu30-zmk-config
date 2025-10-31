# uwu30 ZMK Repo

## Instructions

Add this repository to your existing `config/west.yml` as shown below. (No idea what that means? [Check this repository instead!](https://github.com/quark-works/uwu30-user-config))

```yaml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    # Add the base GitHub URL as a remote.
    - name: quark-works # You can name this whatever you like; just make sure the "remote" below matches.
      url-base: https://github.com/quark-works
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    # Add the name of the repository as a project.
    - name: uwu30-zmk-config
      remote: quark-works
      revision: main # This is the name of the branch you want to use.
  self:
    path: config
```

After doing so, add a copy of [the default keymap](boards/arm/uwu30/uwu30.keymap) and create a `uwu30.conf` file `config` folder that is already in your repo. You can take a look at the [user repo](https://github.com/quark-works/uwu30-user-config) for an example.
