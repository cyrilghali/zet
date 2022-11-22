# Handlers & Notify - Ansible

Let's suppose you want to run a task if an event happen while executing your
Ansible playbook. You'll use `handler` and `notify`

Example

```
- name: Enable Apache rewrite module (required for Drupal).
   apache2_module: name=rewrite state=present
   notify: restart apache
```

```
handlers:
  - name: restart apache
     service: name=apache2 state=restarted
```
