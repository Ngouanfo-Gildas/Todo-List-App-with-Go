# Command Line To-Do List Application

## Introduction

The goal of this project is to developpe a ***Command Line To-Do List Application*** in C  and GO programming langage. This application will enable users to manage their tasks list efficiently in Command Line mode, without having to bother with overy sophisticated tools.

## Main functionalities

Application must include the following features:

| Feature    | Function name|    Description    |
|:-----------|-----:|:------------------------|
| Add task | **add_task** | User can add new task in tasks list.|
| List tasks list | **list_tasks**| User can list a tasks list. |
| Delete task | **delete_task** | User can delete task specifiyng its ID |
| Edit task | **edit_task** | User can edit specified field of a task. |
| Edit task status | **edit_task_status** | User can change task status making it Done or Left. |
| View task details | **more_about_task** | This help user to view all the fields of a specified task. |

## Data specification

The main data we handling in this app is **TASK**. A task is define by:
| | Variable name| Variable description |
|-------|--------: |-------------- |
| Task name | **name** | defines the name on the task. |
| Task status | **status** | Define the status of the task (Done or Left). |
| Task priority | **priority** | Defines the priority of the task (betwen 0 to 15). |
| Task estimated time | **estimated_time** | Defines the number of minutes the task will be realize. |
| Task creation date | **creation_date** | Defines the cration date of the task. |
| task to-do date | **date** | Defines the date on which the task is to be performed. |
| Task due time | **due_time** | Defines the date by which the task must be completed at the latest. |
| Task comment | **comment** | Defines a comment of the task. Most ressources that help to done task. |

> Each variable value must be validate before storage to ensure data integrity.

### Task Structure

```C
// Structure de la tâche
typedef struct {
    cahr **name;
    char status; // "Done" ou "Left"
    int priority;   // 0 to 15
    int estimated_duration; // maximum of 90 minutes
    char date[11];  // Format: "YYYY-MM-DD"
    char due_date[11]; // Format: "YYYY-MM-DD"
    char **comment;
} Task;
```

## Technical constraints

- App must write in C or Go porgramming langage.
- User Interface must be Command Line.
- All about tasks must be store in text file.

## Function prototypes

```h
//* Add a task*/
void add_task(Task* task_list, int* num_tasks);

/* Delete a task */
void delete_task(Task* task_list, int* num_tasks);

/* Edit a task details */
void edit_task(Task* task_list, int num_tasks);

/* Display the tasks list*/
void list_tasks(Task* task_list, int num_tasks);

// Mark task as done */
void task_ended(Task* task_list, int num_tasks);

// Display details about a specific task */
void more_about_task(Task* task_list, int num_tasks);
```

## Command Line Architecture

```bash
task add 

task list

task edit status ok <task-id>

task delete <task-id>

task view <task-id>
```

## Deliverable

f
