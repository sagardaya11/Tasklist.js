# Tasklist.js
import React from 'react'

function TaskList({tasks,deleteTask ,editTask ,toggleTask}) 
{
  return (
  
       <ul> {tasks.map((task, index) => (
        <li key={index}>
            <span onClick={()=>toggleTask(index)}
                style={{
              textDecoration: task.completed ? "line-through" : "none",
              cursor: "pointer",
              marginRight: "10px",
            }}>
                {task.text}
            </span>

            <button onClick={()=>editTask(index)}>Edit</button>
            <button onClick={()=>deleteTask(index)}>Delete</button>
        </li>
     )  )}
   
        </ul>      
        
    
  );
}

export default TaskList;
