## Welcome to GitHub Pages

import csv
import cx_Oracle

print(datetime.datetime.now())

#Oracle portion of the script
sql = '''select [columns] from [table] where [condition]''' 
oracle_cursor.execute(sql)

print(datetime.datetime.now())

#SQLite portion of the script
sqlite_conn.executeany('''INSERT into [table] 
                          ([columns]) 
                          values (?,?,?...etc.)''', 
                          oracle_cursor
                       )
sqlite_conn.commit()
sqlite_conn.close()

