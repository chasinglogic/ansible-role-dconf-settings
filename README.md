dconf_settings
==============

Use variable files to specify GNOME settings (and settings for other things that use gsettings)


Role Variables
--------------

This module has a single variable that is required `dconf_settings`. This is a list of YAML dictionaries specifying the dconf key and value like so:

```yaml
dconf_settings:
  # Set CAPSLOCK as Ctrl
  - key: org.gnome.desktop.input-sources.xkb-options
    value: "['ctrl:nocaps']"
```

Optionally you can specify a descriptive name for the setting to be displayed by Ansible:

```yaml
dconf_settings:
  - name: Set CAPSLOCK as Ctrl
    key: org.gnome.desktop.input-sources.xkb-options
    value: "['ctrl:nocaps']"
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - chasinglogic.dconf_settings
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
