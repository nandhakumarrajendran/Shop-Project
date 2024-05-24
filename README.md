<h1>ONLINE MENU FOR SHOP</h1>
<ul type="disc">
  <li>Create a New Folder for the Project on the Desktop named a Shop-Project.</li>
  <li>Open the Shop-Project folder in cmd and create a virtual environment for this project. It is used to contain specific Python libraries and Packages that are needed to support a project.<br>
  using this,
    <ul>
      <h3><code>py -m venv <span title="folder name">Env</span></code></h3>
      <div>
          <h3><blockquote><code> C:// Users/ User/ Desktop/ Shop-Project>py -m venv Env </code></blockquote></h3>
      </div>
      <li><b>Env</b> is a Folder Name of Virtual Environment.</li>
      <li>Before that we want to install a virtual environment on the desktop. <br><h3> <code>pip install virtualenv</code></h3></li>
    </ul>
    </li>
    <li>After creating a virtual environment we want to install some needed packages and libraries for a project.</li>
    <li>For that we want to go <tt>Scripts</tt> and <tt>Activate</tt>.</li>
    <div>
      <h3><blockquote><code> C:// Users/ User/ Desktop/ Shop-Project/ Env/ Scripts> Activate </code></blockquote></h3>
    </div>
  <li>In this Project we have used a Django web framework so we want to install Django inside a <tt>Scripts</tt>.</li>
  <ul>
    <h3><code>pip install django</code></h3>
  </ul>
<li>After this we can see that version by using,</li>
  <ul>
    <h3><code>django-admin --version</code></h3>
  </ul>
<li>After installing our packages we want to create a Project.</li>
<li>Now, we want to create a project,</li>
  <ul>
    <h3><code>django-admin startproject <span title="folder name">Project</span></code></h3>
    <h3><blockquote><code> C:// Users/ User/ Desktop/ Shop-Project> django-admin startproject Project </code></blockquote></h3>
    <li><b>Project</b> is a folder name of project.</li>
  </ul>
<li>In this project we have two sides one is the Admin side and another one is the Customer side. for that, we want to create two Apps by using this command line.</li>
  <ul>
    <h3><code>py manage.py startapp <span title="folder name">Admin</span></code></h3>
    <h3><code>py manage.py startapp <span title="folder name">Customer</span></code></h3>
    <li>like this,</li>
    <h3><blockquote><code> C:// Users/ User/ Desktop/ Shop-Project/ Project> py manage.py startproject Admin </code></blockquote></h3>
  </ul>

<li>We can run the server using,</li>
 <ul>
   <h3><code>py manage.py runserver</code></h3>
 </ul>
 <li>After Creating Apps we want to add to the Installed Apps list at  files.</li>
 <ul><h3>
   INSTALLED_APPS = [ <br>
                   ....,<br>
                   ....,<br>
                'Admin',<br>
             'Customer',<br>
]
 </h3></ul>
 <li>Next we want to create a <tt>Templates</tt> folder and a <tt>Static</tt> Folder.</li>
 <ul>
   <li>Templates Folder is used to store <b>HTML</b> files for the Specific Project.</li>
   <li>Static Folder is used to store <b>CSS</b> files, <b>JavaScript</b> files, and <b>Images</b> for the Specific Project.</li>
   <li>After creating these folders we want to configure our folder in <tt>Settings.py</tt>.</li>
   <li>Templates config,
     <h3><code>TEMPLATES = [</code><br>
     <code>    {</code><br>
     <code>        ......,</code><br>
     <code>        DIRS:  [os.path.join(BASE_DIR, "templates")]</code><br>
     <code>        ......,</code><br>
     <code>     }</code><br>
   <code>]</code></h3></li>

   <li>Static config,
     <h3><code>STATIC_URL = 'static/'</code><br>
       <code>STATICFILES_DIRS = [os.path.join(BASE_DIR, STATIC_URL)]</code><br>
       <code>STATIC_ROOT = os.path.join(BASE_DIR,'STATICFILES_DIRS')</code></h3>
   </li>
 </ul>
 <li>After Configuring all these folders we want to create separate <tt>urls.py</tt> files for each Apps.</li>
 <li>After creating we want to configure these Urls to project urls.py </li>
</ul>
