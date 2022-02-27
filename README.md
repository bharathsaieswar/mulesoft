import sqlite3

conn = sqlite3.connect('Bharath.db') 

c = conn.cursor()

def create_table():

    c.execute("CREATE TABLE IF NOT EXISTS stuffToPlot('Movie Name', 'Actor', 'Actress', 'Year of Release', 'Director Name')")

def data_entry():

    c.execute("INSERT INTO stuffToPlot VALUES('Bheemla Nayak','Pawan Kalyan','Nithya Menon','25 feb 2022','Kacheguda')")
    
    conn.commit()
    
    c.close()
    
    conn.close()
    
create_table()

data_entry()
