import { useState } from 'react'
import { DragDropContext, Droppable, Draggable } from 'react-beautiful-dnd'
import initialData from './initial-data'
import Column from './Column'
import LandingPage from './LandingPage'

function App() {
  const [state, setState] = useState(initialData)
  const [showBoard, setShowBoard] = useState(false)

  const onDragEnd = (result: any) => {
    const { destination, source, draggableId } = result

    if (!destination) return
    
    if (
      destination.droppableId === source.droppableId &&
      destination.index === source.index
    ) return

    const start = state.columns[source.droppableId]
    const finish = state.columns[destination.droppableId]

    if (start === finish) {
      const newTaskIds = Array.from(start.taskIds)
      newTaskIds.splice(source.index, 1)
      newTaskIds.splice(destination.index, 0, draggableId)

      const newColumn = {
        ...start,
        taskIds: newTaskIds
      }

      setState({
        ...state,
        columns: {
          ...state.columns,
          [newColumn.id]: newColumn
        }
      })
      return
    }
    
    // Moving from one column to another
    const startTaskIds = Array.from(start.taskIds)
    startTaskIds.splice(source.index, 1)
    const newStart = {
      ...start,
      taskIds: startTaskIds
    }

    const finishTaskIds = Array.from(finish.taskIds)
    finishTaskIds.splice(destination.index, 0, draggableId)
    const newFinish = {
      ...finish,
      taskIds: finishTaskIds  
    }

    setState({
      ...state,
      columns: {
        ...state.columns,
        [newStart.id]: newStart,
        [newFinish.id]: newFinish
      }
    })
  }

  return (
    <>
      {!showBoard ? (
        <LandingPage />
      ) : (
        <DragDropContext onDragEnd={onDragEnd}>
          <div className="app">
            {state.columnOrder.map((columnId) => {
              const column = state.columns[columnId]
              const tasks = column.taskIds.map((taskId: string) => state.tasks[taskId])

              return <Column key={column.id} column={column} tasks={tasks} />
            })}
          </div>
        </DragDropContext>
      )}
    </>
  )
}

export default App