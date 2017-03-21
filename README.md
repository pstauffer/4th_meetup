# 4th_meetup

## gpg commands

```
# list all keys
gpg --list-keys 

# create a key
gpg --gen-key
```

```
# trust key
gpg --edit-key pstauffer@confirm.ch
trust
5
```

## gpg-agent

```
# install gpg-agent via gnupg-agent package
apt-get install gnupg-agent
```

## Use Case

```
# encrypt password
echo test |gpg -r pstauffer@confirm.ch -e -o vault_passphrase.gpg
chmod 600 vault_passphrase.gpg

# define vault password file
export ANSIBLE_VAULT_PASSWORD_FILE=vault.sh

chmod 750 vault.sh
```

## Links

* https://www.digitalocean.com/community/tutorials/how-to-use-gpg-to-encrypt-and-sign-messages-on-an-ubuntu-12-04-vps
* https://benincosa.com/?p=3235

### To Do

* https://dantehranian.wordpress.com/2015/07/24/managing-secrets-with-ansible-vault-the-missing-guide-part-1-of-2/
* http://fishi.devtail.io/weblog/2016/04/02/testing-ansible-ansible-vault-travis-ci/

* http://docs.ansible.com/ansible/playbooks_best_practices.html#variables-and-vaults
* http://docs.ansible.com/ansible/playbooks_vault.html
