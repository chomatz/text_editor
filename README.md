# text_editor
ansible role for vim provisioning

## requirements

## variables

## dependencies

## examples
```
- name: initialize vimrc generator
  ansible.builtin.include_role:
    name: text_editor
    tasks_from: vimrc_template.yml
```
```
- name: add custom variable(s) to vimrc generator
  ansible.builtin.include_role:
    name: text_editor
    tasks_from: vimrc_injector.yml
  vars:
    vimrc_label: custom_label
    vimrc_type: variable
    vimrc_content: |
      variable_1="value 1"
      variable_2="value 2"
      variable_3="value 3"
```
```
- name: add custom script(s) to vimrc generator
  ansible.builtin.include_role:
    name: text_editor
    tasks_from: vimrc_injector.yml
  vars:
    vimrc_label: custom_label
    vimrc_type: script
    vimrc_content: |
      do domething here
      do something with variable_1 that was defined previously
      do something with variable_2 that was defined previously
      do something with variable_3 that was defined previously
      do another thing here
```
