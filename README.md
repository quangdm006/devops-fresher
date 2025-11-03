# DEVOPS FRESHER

## CI/CD

### CI/CD là gì?
  - Được chia thành 2 phần : CI và CD
  - CI = Continous Integration
  - CD = Continuos Deployment : triển khai hoàn toàn tự động
  - CD = Continous Delivery : triển khai thủ công 
  - Công cụ : Gitlab CI/CD và Jenkins

## Cài đặt Gitlab server



## Gitlab CI/Continuos Deployment
  1. Cài đặt công cụ tự động:
    - Gitlab runner

  2. Viết file cấu hình công việc:
    - Viết trực tiếp trong dự án , định dạng file : .gitlab-ci.yml

  **Bước 1 : Cài đặt gitlab-runner:**
    1. Search từ khóa : how to install gitlab runner on ubuntu 20.04 

    2. Sử dụng câu lệnh : curl -L "https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh" | sudo bash , để add repo gitlab
    
    3. Cài đặt phiên bản mới nhất của gitlab-runner: sudo apt install gitlab-runner và apt-cache madison gitlab-runner