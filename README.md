# ansible-roles

```
sudo yum install git -y


git clone https://github.com/amedio77/ansible-roles

cd ansible-roles/

# ansible 설치 및 pem 파일 생성
./install-env.sh


#ip 변경
$ vi roles/hosts_autopass/templates/hosts.j2
10.0.0.x hmaster
10.0.0.x hworker-1
10.0.0.x hworker-2


# ansible role 실행

ansible-playbook --private-key ~/.ssh/kepri-msa.pem  hosts_autopass_roles.yml --skip-tags workers,master

ansible-playbook --private-key ~/.ssh/kepri-msa.pem  hosts_autopass_roles.yml -t master --skip-tags workers

ansible-playbook --private-key ~/.ssh/kepri-msa.pem  hosts_autopass_roles.yml -t workers --skip-tags master

```
