# DEVOPS FRESHER

## CI/CD

### CI/CD là gì?
  - Được chia thành 2 phần : CI và CD
  - CI = Continous Integration
  - CD = Continuos Deployment : triển khai hoàn toàn tự động
  - CD = Continous Delivery : triển khai thủ công 
  - Công cụ : Gitlab CI/CD và Jenkins

## Cài đặt Gitlab server

  1. Nên tạo 1 server khác cho gitlab server:

    - vì gitlab server sẽ sử dụng nhiều port khác
    
    - snapshot từ ubuntu origin , sau khi snapshot thì vào /etc/netplan/00-installer-config.yaml config lại cấu hình và đổi tên hostname cho server
  
  2. Search gitlab ee packages và cài đặt :

    1. Tải repo :

      Sử dụng câu lệnh : curl -s https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/script.deb.sh | sudo bash

    2. Download : 

      Sử dụng câu lệnh : apt-get install gitlab-ee=14.4.1-ee.0

    3. Thêm hosts để có thể truy cập server qua DNS

      - 192.168.222.131 git.quangdm.test

    4. Mở file /etc/gitlab/gitlab.rb

      - sửa địa chỉ external_url 'http://git.quangdm.test'

    5. Chạy câu lệnh :

      gitlab-ctl reconfigure

    6. Vào máy windows : 
    
    C:\Windows\System32\drivers\etc\hosts cấu hình hosts

    - Tài khoản mặc định : root 
    - mật khẩu sử dụng câu lệnh : cat /etc/gitlab/initial_root_password

    7. Edit profile để đổi mật khẩu

## Gitworkflow

  - 


## Gitlab CI/Continuos Deployment
  1. Cài đặt công cụ tự động:

    - Gitlab runner

  2. Viết file cấu hình công việc:

    - Viết trực tiếp trong dự án , định dạng file : .gitlab-ci.yml

  **Bước 1 : Cài đặt gitlab-runner:**

    1. Search từ khóa : how to install gitlab runner on ubuntu 20.04 

    2. Sử dụng câu lệnh : curl -L "https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh" | sudo bash , để add repo gitlab

    3. Cài đặt phiên bản mới nhất của gitlab-runner: sudo apt install gitlab-runner và apt-cache madison gitlab-runner