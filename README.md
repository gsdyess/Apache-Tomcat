# Apache-Tomcat

Steps tacken to acheve the end results:

  1.created directory: chef_tomcat
  
  2.created in nano INSTRUCTIONS.rd file:
  
     contents of file: 
     
          package 'httpd'

          service 'httpd' do
             action [:enable, :start]
          end
  3. created a template: $ chef generate template cookbooks/learn_chef_httpd index.html   
  
  4. Update the recipe to reference the html template
      Write out the recipe to default.rb
  5. Run the cookbook $ sudo chef-client --local-mode --runlist 'recipe[apache_http]'
  
  6. $ curl localhost
  
Build and test process
  Built on AWS CentOS 7.4 (VM Image 1)
  Tested on AWS CentOS 7.4 (VM Image 2)
  
Tools and resources used in the process:
  - AWS CentOS VM IMages: 1 vm for development and 1 for testing
  - Nano editor
  
  Resources: 
  - Chef Rally site
  - Chef Documentation
  - Google search 
       
Run on node:
  1. Git clone from https://github.com/gsdyess/Apache-Tomcat.git
  
  2.Create cookbook: $ sudo chef-client --local-mode --runlist 'recipe[apache_http]’
  
  3.Run: $. curl local host
