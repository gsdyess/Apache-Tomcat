# Apache-Tomcat

Steps tacken to acheve the end results:

  1.created directory: chef_tomcat
  
  2.created in nano INSTRUCTIONS.rd file:
 
          package 'httpd'

          service 'httpd' do
             action [:enable, :start]
          end
          
  3. test out INSTRUCTIONS.rb: $ sudo chef-client --local-mode INSTRUCTIONS.rb  
  
  4. Start and enable the Apache service: 
  
  5. Add a home page: sudo chef-client --local-mode INSTRUCTIONS.rb
  
  6. Confirm your web site is running: $ curl localhost
  
  7. Create a cookbook: apache_http
  
  8. Generate cookbook: $ chef generate cookbook cookbooks/learn_chef_httpd
          
  9. created a template: $ chef generate template cookbooks/learn_chef_httpd index.html   
  
  10. Update the recipe to reference the html template
      Write out the recipe to default.rb
  11. Run the cookbook $ sudo chef-client --local-mode --runlist 'recipe[apache_http]'
  
  12. $ curl localhost
  
Build and test process
  Built on AWS CentOS 7.4 (VM Image 1)
  Tested on AWS CentOS 7.4 (VM Image 2)
  
Tools and resources used in the process:
  - AWS CentOS VM IMages: 1 vm for development and 1 for testing
  - Nano editor
  - git
  
  Resources: 
  - Chef Rally site
  - Chef Documentation
  - Google search 
       
Run on node:
 1. Git clone from https://github.com/gsdyess/Apache-Tomcat.git
  
  2. Create cookbook: $ sudo chef-client --local-mode --runlist 'recipe[apache_http]’
  
  3. Run: $. curl local host
