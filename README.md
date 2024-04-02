## Usage

1. Setup bash completion script, there are two types of auto completion you can choose from.

   * start with an action and followed by options

     ```bash
     # actions
     local action_list=( ... )

     # options for each action
     local option_bool_<action>=( ... )      # on/off option
     local option_file_<action>=( ... )      # followed by file
     local option_files_<action>=( ... )     # followed by files
     local option_argument_<action>=( ... )  # followed by argument
     local option_arguments_<action>=( ... ) # followed by arguments

     # arguments for each option
     # (remove all non-alphanumeric characters from option)
     local argument_list_<option>=( ... )
     ```

   * options only

     ```bash
     # options
     local option_bool=( ... )      # on/off option
     local option_file=( ... )      # followed by file
     local option_files=( ... )     # followed by files
     local option_argument=( ... )  # followed by argument
     local option_arguments=( ... ) # followed by arguments

     # arguments for each option
     # (remove all non-alphanumeric characters from option)
     local argument_list_<option>=( ... )
     ```

2. Replace \<###> with a unique string. (ex: command name)

3. Install bash completion script.

   * for all users

     ```shell
     $ sudo mkdir -p /usr/share/bash-completion/completions
     $ sudo cp <bash completion script> /usr/share/bash-completion/completions/<command name>
     ```

   * for single user

     ```shell
     $ mkdir -p ~/.local/share/bash-completion/completions
     $ cp <bash completion script> ~/.local/share/bash-completion/completions/<command name>
     ```