* Simple ansible playbook for deploying my blog

<pre>
ssh-keygen
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
git clone https://github.com/dan-v/pelican-blog-ansible
# copy over missing ssl certificate files at roles/common/files
apt-get update
apt-get install python-pip python-dev git -y
pip install PyYAML jinja2 paramiko ansible
cd pelican-blog-ansible
ansible-playbook -i hosts site.yml
</pre>
