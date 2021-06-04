# django auto reload on custom file change

# Setup Instruction

1. Create directory structure in your app.
   `PROJECT_NAME/APP/management/commands/`
2. Copy the files `autoreload.py`, `runapp.py`& `server_command.py` inside `commands` directory.
3. Add `CUSTOM_FILE_MONITOR` attribute in `settings.py`.
   *** CUSTOM_FILE_MONITOR=[os.path.join(BASE_DIR, 'PROJECT_NAME', 'config.json')] ***
   Exp. to monitor config.json file changes restart server.

# Scenario

If you have to monitor file changes like configuration switch from 
development to production of any credentials changes and you want to restart server auto.

Example. Here I am using djang-admin to change config.json file directly from admin panel and auto restart server.

# Compatible with Django>=3.1.1

