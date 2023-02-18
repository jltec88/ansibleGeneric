To run using the command:
ansible-playbook -i ./inventory -e servers=group_aa ./playbook.yml --vault-password-file ./group_vars/all/.vault_password.txt

And you can use the following command to revert what was done with the previous playbook:
ansible-playbook -i ./inventory -e servers=group_aa ./playbook_rollback.yml --vault-password-file ./group_vars/all/.vault_password.txt


To edit the Vault file
ansible-vault edit ./group_vars/all/vault.yml
The password of this Vault file is: 111

You can change the password of the Vault file with:
ansible-vault rekey ./group_vars/all/vault.yml

or 

You can create a new Vault file:
ansible-vault create ./group_vars/all/new_vault.yml

Regards,