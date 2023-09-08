# CreateUser-AWSEC2
Create a new user in AWS EC2 instance and set up password

Change Password for existing User
- Edit the sshd configuration file /etc/ssh/sshd_config as root.
- Find the parameter PasswordAuthentication. Make sure it's uncommented and set to yes.
- And then generate the password for the user with the command ‘sudo passwd user_name’

<img width="568" alt="Screenshot 2023-09-08 at 3 15 11 PM" src="https://github.com/ekoride/CreateUser-AWSEC2/assets/94488604/df305bd9-c9a4-4678-81c5-e3dff960420e">

Create a new User with Password
- Create a new user with below command 'sudo adduser new_user'
- Then fire the below command to edit the parameter PasswordAuthentication. Make sure it's uncommented and set to yes. 'sudo vi /etc/ssh/sshd_config'
- After above step, fire the command 'sudo service sshd restart'
- And then generate the password for the user 'sudo passwd new_user'
