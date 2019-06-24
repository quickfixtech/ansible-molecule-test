# ansible-molecule-test

sudo apt-get update
sudo apt-get install -y python-pip
python -m pip install virtualenv
python -m virtualenv my_env
source my_env/bin/activate
python -m pip install molecule docker


molecule init role -r ansible-apache -d docker
cd ansible-apache
molecule test
