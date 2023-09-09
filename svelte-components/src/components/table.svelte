<!-- Table.svelte -->
<script>
    // Import the necessary components and data
    import { Table, Column } from 'svelte-table';
    import data from './data'; // Your data source

    // Define the columns for your table
    const columns = [
        new Column('Name', 'name'), // Replace 'name' with the actual field name from your data
        new Column('Age', 'age'),   // Replace 'age' with the actual field name from your data
        // Add more columns as needed
    ];
</script>

<Table {columns} {data}>
    <!-- You can add any custom table UI here, e.g., pagination -->
</Table>
