from collections import deque

# Different graph (city navigation example)
city_map = {
    "Home": ["School", "Market"],
    "School": ["Library", "Playground"],
    "Market": ["Hospital"],
    "Library": [],
    "Playground": ["Hospital"],
    "Hospital": []
}

# BFS (iterative, returns shortest path)
def bfs_path(graph, start, goal):
    queue = deque()
    queue.append((start, [start]))
    visited = set()

    while queue:
        current, path = queue.popleft()

        if current == goal:
            return path

        if current not in visited:
            visited.add(current)
            for neighbor in graph[current]:
                queue.append((neighbor, path + [neighbor]))

    return None


# DFS (using stack instead of recursion)
def dfs_path(graph, start, goal):
    stack = [(start, [start])]
    visited = set()

    while stack:
        current, path = stack.pop()

        if current == goal:
            return path

        if current not in visited:
            visited.add(current)
            for neighbor in graph[current]:
                stack.append((neighbor, path + [neighbor]))

    return None


# Run example
start_node = "Home"
goal_node = "Hospital"

print("BFS Route:", bfs_path(city_map, start_node, goal_node))
print("DFS Route:", dfs_path(city_map, start_node, goal_node))
