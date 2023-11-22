# Initial User Ansible Role

This role, checks if it can connect with the Ansible User and update SSH authorized keys for it.
If it cannot connect, it will try to connect with `initial_user` and create `ansible_user`.

## Usage

To use this role, `gather_facts` must be disabled at playbook level.

| Variable                | Effect                                                                                                                   |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `initial_user`          | The user used for connection, if `ansible_user` doesn't work. The user will be deleted afterwards. (Defaults to `root`) |
| `ansible_user`          | The normal ansible connection user                                                                                      |
| `ansible_user_pubkeys`  | Public keys, to deploy on `ansible_user`                                                                                |
| `remove_initial_user`   | Wether `Initial_User` should be deleted afterwards. (Defaults to `false`)                                               |
| `ansible_user_password` | Password to set for ansible user. __Optional__                                                                              |
