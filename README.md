## nieldejonghe.com
Repository for holding my resume website contents and raspberry pi configurations.

### Project details:

**Must Have**

- Setup VPN on PI so I can safely connect to it from outside my home network (Wireguard and forward VPN port)
- Hosting the website will happen on my RPI4 from my home.
- RPI and webserver configuration should happen with an ansible playbook.
- Need DNS hosting of nieldejonghe.com, how to make sure dynamic IP is updated?
- Look into fail2ban as website will be public.
- Next to fail2ban look into other security best practices.
- Generate static html pages with the help of HUGO.
- Host website with nginx.
- Initial contents of the page should be my own resume.
- CI/CD should push updates upon commit to main branch to *production*.
- Look into port forwarding configration on local router (80 and 443 most likely)
- Document all efforts.
- How to deal with secrets when using a public git repo?

**Nice to have**

- Some monitoring dashboard, grafana?
- Provide additional content to website: 
  - <insert ideas here>
  - ...
  - play around with chatbot?
  - Self created documenting tool with markdown?
- Setup automatic OS patching
- Setup vulnerability scanner 
- Find a way to visiualize cicd steps that build this website (Maybe in realtime?) 
- Add website visitor counter (write to db?)
- Extend ban period in fail2ban and reverse IP lookup locations (maybe show graphical on site?)
  
### Configuration Steps

**Raspberry Pi setup**

1. Start from a clean RPI, install latest OS and update.
2. Ansible configuration for nginx and creating hello world website

- On your DEV machine Install Ansible by using virtualenv.

    ```
    sudo apt update && sudo apt install -y sshpass python3-pip python3-venv # installing needed packages
    python3 -m venv ~\ansible # creating virtualenv
    source ~/ansible/bin/activate # starting virtualenv
    python3 -m pip install ansible # installing ansible
    ansible --version # checking ansible version
    ```

- Setting up Ansible to connect to raspberry pi.

    ` ansible-playbook pi-setup.yml --ask-pass --diff `






