## ![stored.programs logo](https://raw.githubusercontent.com/deepgrace/stored.programs/master/logo/stored.programs.png)
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)
## Stored Programs (Function, View, Trigger and Stored Procedure) in SQL

## Overview

## factorial
```sql
-- SET max_sp_recursion_depth = N

DROP PROCEDURE IF EXISTS factorial;
DELIMITER //
CREATE PROCEDURE factorial(n INT, OUT f INT)
BEGIN
       IF n <= 1 THEN
          SET f = 1;
       ELSE
          CALL factorial(n-1, @k);
          SET f = n * @k;
       END IF;
END //
DELIMITER ;
```
