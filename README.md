shadcn-ui is a collection of components built with radix-ui.\
https://ui.shadcn.com/

The Data Table component is built with @tanstack/react-table.\
https://ui.shadcn.com/docs/components/data-table\
https://tanstack.com/table/v8

This repo copies the tasks example into a new nextjs project.

The goal is to provide a collection of table examples.

Here are the steps I took to build it:
1. Install nextjs: npx create-next-app@latest
2. Install shadcn-ui: npx shadcn-ui@latest init
3. Clone shadcn-ui repo, copy tasks example directory to /src/app/
4. Copy layout.tsx, remove unused components.
5. Modify page.tsx, remove unused components, check the copied components as well.
6. Install shadcn components according to errors that appear.
7. Fix lines that reference incorrect paths like /registry/new-york to /components
8. Fix link to DataTableViewOptions
9. Fix data imports

# Initial page size
The default number results per page is 10.

To Change it, set initialState.pagination.pageSize in the table options.
```
const table = useReactTable({
  data,
  columns,
  state: {
    sorting,
    columnVisibility,
    rowSelection,
    columnFilters,
  },
  initialState: {
    pagination: {
      pageSize: 20
    }
  }
})
```
https://tanstack.com/table/v8/docs/api/core/table#initialstate\
https://tanstack.com/table/v8/docs/guide/pagination\
https://ui.shadcn.com/docs/components/data-table#pagination
