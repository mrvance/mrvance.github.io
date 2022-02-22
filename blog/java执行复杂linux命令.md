## 用Runtime.getRuntime().exec(cmds)在执行复杂命令时报错，需要按以下方式执行
```
String cmd = "ps -ef|grep java";
String[] cmds = new String[]{"sh","-c",cmd};
Process process = Runtime.getRuntime().exec(cmds);
while ((line = reader.readLine()) != null) {
  System.out.println(line);
}
    		
注意"sh","-c"参数
