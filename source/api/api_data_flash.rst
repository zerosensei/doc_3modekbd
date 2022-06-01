Data flash
############

DATA FLASH管理使用的是开源项目 `EasyFlash <https://github.com/armink/EasyFlash>`_。这里只介绍常用API。

初始化dataflash
==================

- 函数名

 ``EfErrCode easyflash_init(void)``

- 参数

  +--------+----------------+
  | param  | description    |
  +========+================+
  | return | `0` on success |
  +--------+----------------+



写入数据到dataflash
======================

- 函数名

  ``EfErrCode ef_set_env_blob(const char *key, const void *value_buf, size_t buf_len)``

- 参数

  +-----------+------------------+
  | param     | description      |    
  +===========+==================+
  | key       | ENV name         |
  +-----------+------------------+
  | value_buf | ENV value        |
  +-----------+------------------+
  | buf_len   | ENV value length |
  +-----------+------------------+
  | return    | `0` on success   |
  +-----------+------------------+



读取dataflash
==================

- 函数名

  ``size_t ef_get_env_blob(const char *key, void *value_buf, size_t buf_len, size_t *saved_value_len)``

- 参数

  +-----------------+-----------------------------------------------------------------+
  | param           | description                                                     |
  +=================+=================================================================+
  | key             | ENV name                                                        |
  +-----------------+-----------------------------------------------------------------+
  | value_buf       | ENV blob buffer                                                 |
  +-----------------+-----------------------------------------------------------------+
  | buf_len         | ENV value length                                                |
  +-----------------+-----------------------------------------------------------------+
  | saved_value_len | return the length of the value saved on the flash, 0: NOT found |
  +-----------------+-----------------------------------------------------------------+
  | return          | the actually get size on successful                             |
  +-----------------+-----------------------------------------------------------------+


