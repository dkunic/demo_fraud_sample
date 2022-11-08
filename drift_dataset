# -------------------------------------------------------------------------------- NOTEBOOK-CELL: CODE
import dataiku
import pandas

# -------------------------------------------------------------------------------- NOTEBOOK-CELL: CODE
drift_dataset = dataiku.get_custom_variables()["DRIFT_DATASET"]

# -------------------------------------------------------------------------------- NOTEBOOK-CELL: CODE
my_dataset = dataiku.Dataset("transactions_demo_joined_prepared")
df = my_dataset.get_dataframe()

# -------------------------------------------------------------------------------- NOTEBOOK-CELL: CODE
#df.authorized_flag.describe()

# -------------------------------------------------------------------------------- NOTEBOOK-CELL: CODE
#df.authorized_flag_new.describe()

# -------------------------------------------------------------------------------- NOTEBOOK-CELL: CODE
if drift_dataset == 'True': df.authorized_flag=df.authorized_flag_mod

# -------------------------------------------------------------------------------- NOTEBOOK-CELL: CODE
output_ds = dataiku.Dataset("transactions_python2")
output_ds.write_with_schema(df)
