<h1>Compute Grid Resources</h1>

<p>Compute Grid is a peer-to-peer GPU Resource Marketplace offering inexpensive and fully virtualized GPU instances.</p>
<p>We also pride ourselves in being easy to use and beginner friendly. One of the ways we do that is by offering public resources, such as this one.</p>
<p>Here you will find information on how to securely move files to and from your instance, how to upload custom models to ComfyUI and more.</p>
<p>For more resources and tutorials visit our <a target="_blank" href="https://www.youtube.com/@compute-grid">YouTube channel</a>.
<br />

<h2>How to upload custom SDXL Models</h2> 
<p> To install custom SDXL models or models not found in the manager or our shared folder, follow the below directions: </p>

<ol>
    <li> Using your terminal SSH into your instance using the provided SSH commands. </li>
    <li> Use the <b>"cd ComfyUI/"</b> command to access the ComfyUI folders.</li>
    <li> <b>"cd models"</b> </li>
    <li> Use the <b> "ls" </b> command to display the different model folders. </li>
    <li> Once you find the proper model folder, run <b>"cd <i>proper_model_folder</i>"</b>.</li>
    <li> Now inside of the model folder run <b>"wget <i>model_download_link</i>"</b> to begin model install. </li>
    <li> Once installed you may need to change the model name to one that is useable, using the <b>"mv <i>Old_file_name</i> <i>New_file_name</i>"</b>
</ol>
<br />


<h2>How to securely transfer files on Compute Grid</h2>
<p>There maybe a time you will need to transfer files from your private instance to your personal machine, or vice versa. To do so, follow the below directions: </p>

<p>You may need 2 terminal windows to do this. One will be for your personal local machine, that we will refer to as "local", and the other will be for your GPU instance, that we will simply refer to as "instance".</p>

<ol>
<li> Open 2 terminal windows; One will be your local, the other will be for your instance.</li>

<li> SSH into your instance using the SSH Command & Password. <li>

<li> In your instance, locate either the desired Transfer file or the desired file location, depending on your desired action. </li>

<li> In your <u>local</u> terminal, type one of these commands:
    <ul>
        <li> To transfer 1 file from instance to local: <br />
            <b>"scp -P <i>port#</i> cg@computegrid:<i>path/to/source/file</i> ."</b> (Use " ." if you are already inside the desired location on your local machine, or replace it with <b>"path/to/desired/location"</b>) </li>
        <li> To transfer & rename an entire folder from instance to local: <br />
            <b>"scp -r -P <i>port#</i> cg@computegrid:<i>path/to/folder newFolderName</i>"</b> (Only if you are already inside of your desired location)</li>
        <li> To transfer 1 file from your local to your instance: <br />
            <b>"scp -P <i>port# path/to/file/relativeToCurrentLocation</i>  cg@computegrid.ai:<i>path/to/desired/location</i>"</b></li>
    </ul>
</li>

<li> Enter in SSH Password </li>
</ol>
